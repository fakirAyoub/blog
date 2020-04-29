---
title: "Building a CI/CD pipeline for a Spark project using Github Actions, SBT and AWS S3 — Part 2"
date: 2020-04-29T13:01:24+02:00
tags: [aws, s3, github, githubactions]
---
In the [first article](https://medium.com/alterway/building-a-ci-cd-pipeline-for-a-spark-project-using-github-actions-sbt-and-aws-s3-part-1-c7d43658832d) of this series, we talked about how we can set up a CI/CD pipeline for a Spark project using Github Actions, SBT as a build tool and S3 for deployment. Our code once pushed to the [master] branch of our project on Github, triggered an SBT Build command to generate a fat jar, then pushed it to S3 to the chosen bucket.

However, this pipeline still lacks a way to add a logic since it does not allow us to check whether the jar’s version we’re putting to S3 already exists for instance.

To add a similar logic (or expand it if necessary), we have to create our own Github Action. This article aims to show you step by step how we can write a custom Github Action (and publish it!) for our previous CI/CD.

------

In the official [documentation](https://help.github.com/en/actions/building-actions), we see that we can create several types of Github actions; the one that is of interest to us for this article is through [**Creating a Docker container action**](https://help.github.com/en/actions/building-actions/creating-a-docker-container-action)**.**

The first step is to create a Dockerfile that will allow us to run AWS commands through the AWS CLI (also note that we can use boto3 as well for more complex actions like creating an EMR Cluster and running the newly-deployed jar).

In our example, we will check whether the Jar we want to upload already exists in our S3 bucket and if yes, stop the CI part of the pipeline and don’t upload the new jar that we build.

First, we need a Dockerfile that will look like the following:

https://gist.github.com/fakirAyoub/36123741b3cfd458b1bbafaf96f2bf4d

Second, an entrypoint.sh script will help us implement our logic:

https://gist.github.com/fakirAyoub/428074eff73acd7f27d801c72ae9bbf1

Our entrypoint.sh script will check whether the jar exists in the S3 bucket, then run a simple if/else logic. Of course, our AWS Access Key and Secret Access would be stored in Github’s secrets, as we saw in part 1 of this series.

Then, we can create our workflow.yml file as merely as the one we created in the previous article while changing the path to our Github repository since it’s our own Github Action.

https://gist.github.com/fakirAyoub/d8de1acb977fef457fe71ba641113cdb

All set! Finally, it’s better to create a README.MD file to let people know how to use your action.

Then, we push everything to our repository while tagging our release:

```
git add .
git commit -m "My Awesome Github Action"
git tag -a -m "First version OK" v1
git push --follow-tags
```

Voilà! If you’re happy with the Github Action you just created, you can publish it to the official Github Marketplace. Github shows us a step-by-step how-to [here](https://help.github.com/en/actions/building-actions/publishing-actions-in-github-marketplace).
