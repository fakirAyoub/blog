---
title: "Building a CI/CD pipeline for a Spark project using Github Actions, SBT and AWS S3 — Part 1"
date: 2020-04-08T04:35:59+02:00
tags: [aws, s3, spark, sbt, githubactions]
---
Github now allows us to build continuous integration and continuous deployment workflows for our Github Repositories thanks to Github Actions, for almost all Github plans.

In this tutorial, we’re going to go through building a CI/CD pipeline based on a Scala / Spark project. We will be using SBT, the Scala Build Tool, which will allow us to get a jar that we’re then going to deploy to AWS S3 using a custom Github Action.

The first step is to create a Scala (SBT based) project. We will be doing this using the Intellij Idea IDE, but feel free to use your editor / CLI of choice.

First, select File -> New Project and select Scala then sbt.

![Create a Project based on SBT](https://miro.medium.com/max/30/1*XJmWq5S0xg0SNWYAu_6iZg.png?q=20)

![Create a Project based on SBT](https://miro.medium.com/max/1293/1*XJmWq5S0xg0SNWYAu_6iZg.png)

Second, choose a name for your project, and the JDK / SBT / Scala versions.

![img](https://miro.medium.com/max/30/1*vZ0jy2NDqebo_nvbaT3Hzg.png?q=20)

![img](https://miro.medium.com/max/1293/1*vZ0jy2NDqebo_nvbaT3Hzg.png)

For our CI / CD purposes, we would need to generate a *jar* file from our source code as well as our dependencies. To do so, we will need a special plugin called **sbt-assembly**. To do so, under **ProjectName -> project**, create a file called **assembly.sbt** and past the following then save:

<iframe src="https://medium.com/media/8da673c6f8abc5be6a7f19d4aea43b08" allowfullscreen="" frameborder="0" height="65" width="680" title="assembly.sbt" class="z ab ac gs v" scrolling="auto" style="box-sizing: inherit; width: 680px; position: absolute; top: 0px; left: 0px; height: 65px;"></iframe>

Then, you need to add the following dependencies to your **build.sbt** file in project’s root folder:

<iframe src="https://medium.com/media/b919c1465f86a72e8c1711a3333d2a97" allowfullscreen="" frameborder="0" height="483" width="680" title="build.sbt" class="z ab ac gs v" scrolling="auto" style="box-sizing: inherit; width: 680px; position: absolute; top: 0px; left: 0px; height: 483px;"></iframe>

Here we declare our dependencies (by adding them to the libraryDependencies array), then our **assemblyMergeStrategy**, which is the strategy used for our assembly command which plugin was added before (going through the details of this goes beyond the scope of this tutorial, but just add it, it works :))

Finally, all we have to do is write some nice Scala / Spark code in our program. Here is some code that you can put in any package of your structure:

<iframe src="https://medium.com/media/f8f13447c1a960ed8f0335a394eb9f61" allowfullscreen="" frameborder="0" height="307" width="680" title="Main.scala" class="z ab ac gs v" scrolling="auto" style="box-sizing: inherit; width: 680px; position: absolute; top: 0px; left: 0px; height: 307px;"></iframe>

OK, one last step and we’re done! We need to prepare our YAML file that describes the steps that we want to go through in order to get our CI/CD done. To do so, we need to create a folder, namely **.github/workflows**, and inside, create a file (its name does not matter) .yaml:

<iframe src="https://medium.com/media/b766ec9fb28ab1cc7ad5810f4df3b08c" allowfullscreen="" frameborder="0" height="637" width="680" title="ci_cd.yaml" class="z ab ac gs v" scrolling="auto" style="box-sizing: inherit; width: 680px; position: absolute; top: 0px; left: 0px; height: 637px;"></iframe>

Basically, this file gives our CI a name, in our case, “**CI CD”(**innovative, hah?**).**

```
on:
  push:
    branches: [ master ]
```

This tells our workflow that it will be triggered **when** we push some code into the master branch.

```
jobs:
  build:    runs-on: ubuntu-latest
```

Our workflow will run a **ubuntu** image, with the following steps:

1. The first one will setup our JDK, with version 1.8 (same one that we chose when creating the project, remember?)
2. The second one will build our *fat* jar using sbt assembly.
3. Then, we will be using a Github Action, namely **tpaschalis/s3-sync-action@master.** Basically, this step will clone the master’s branch of the Github Action we chose to sync our code to S3. This Action has some parameters, namely: the S3 Bucket we will be uploading our jar to, the AWS ACCESS and SECRET keys, the region, and finally, the ***local\*** path of the jar we want to upload.

Again, our full YAML file will look like:

<iframe src="https://medium.com/media/b766ec9fb28ab1cc7ad5810f4df3b08c" allowfullscreen="" frameborder="0" height="637" width="680" title="ci_cd.yaml" class="z ab ac gs v" scrolling="auto" style="box-sizing: inherit; width: 680px; position: absolute; top: 0px; left: 0px; height: 637px;"></iframe>

The last step here is to define the values of AWS_S3_BUCKET, AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY. For security reasons, these variables need to be hidden securely. For this, Github has a nice feature, namely the **secrets**, where we can defined them:

![img](https://miro.medium.com/max/30/1*Atl_3yNsxuea9Hu8PpmHMw.png?q=20)

![img](https://miro.medium.com/max/1377/1*Atl_3yNsxuea9Hu8PpmHMw.png)

Now all we have to do is to devine our 3 variables (be careful, the names should match with what has been defined in the YAML file), aaaand voilà !

All we have to do now is to push some code into the Master Branch, and magic will happen:

![img](https://miro.medium.com/max/30/1*5lOKewMq8aXnszE7nciaVg.png?q=20)

![img](https://miro.medium.com/max/1581/1*5lOKewMq8aXnszE7nciaVg.png)

Under the **Actions** tab, we find all the steps that our workflow went through, from the build to the deployment to S3.

Hope this tutorial was of a good help to you :)

From Alter Way with love.
