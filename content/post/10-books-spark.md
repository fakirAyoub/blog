---
title: "10+ Great Books for Apache Spark"
date: 2017-01-13T05:45:12+02:00
tags: [spark, books]
---
This article was co-authored by [Matthew Rathbone](https://blog.matthewrathbone.com/)

![img](https://d33wubrfki0l68.cloudfront.net/8177dc9c6ec5935b75460f41e29cecfebe9a5c20/2662a/img/blog/books.jpg)

image by [Ed Robertson](https://unsplash.com/photos/eeSdJfLfx1A)

Apache Spark is a super useful distributed processing framework that works well with Hadoop and YARN. Many industry users have reported it to be 100x faster than Hadoop MapReduce for in certain memory-heavy tasks, and 10x faster while processing data on disk.

While Spark has incredible power, it is not always easy to find good resources or books to learn more about it, so I thought I’d compile a list. I’ll keep this list up to date as new resources come out.

The books are roughly in an order that I recommend, but each has it’s unique strengths.

## [Learning Spark: Lightning-Fast Big Data Analysis](http://amzn.to/2jg01l7)

[![Learning Spark](https://d33wubrfki0l68.cloudfront.net/23703feb00b86493a170c50e13de80988a9dc990/095a6/img/blog/spark-books/1.png)](http://amzn.to/2jg01l7)

*Learning Spark* is in part written by Holden Karau, a Software Engineer at IBM’s Spark Technology Center and my former co-worker at Foursquare. Her book has been quickly adopted as a de-facto reference for Spark fundamentals and Spark architecture by many in the community. The book does a good job of explaining core principles such as RDDs (Resilient Distributed Datasets), in-memory processing and persistence, and how to use the Spark Interactive Shell.

Non-core Spark technologies such as Spark SQL, Spark Streaming and MLib are introduced and discussed, but the book doesn’t go into too much depth, instead focusing on getting you up and running quickly.

Code examples are in Scala and Python.

## [Apache Spark in 24 Hours, Sams Teach Yourself](http://amzn.to/2jFtRfm)

[![Spark in 24 Hours](https://d33wubrfki0l68.cloudfront.net/3a8e1bb340a0f14895a8fbdbad7661af26f865d6/6f247/img/blog/spark-books/2.png)](http://amzn.to/2jFtRfm)

Are you impatient? This book has been written for you!

The first pages talk about Spark’s overall architecture, it’s relationship with Hadoop, and how to install it. You’ll then learn the basics of Spark Programming such as RDDs, and how to use them using the Scala Programming Language. The lasts parts of the book focus more on the *“extensions of Spark”* (Spark SQL, Spark R, etc), and finally, how to administrate, monitor and improve the Spark Performance.

## [High Performance Spark: Best Practices for Scaling and Optimizing Apache Spark](http://amzn.to/2ioCfPs)

[![High performance Spark](https://d33wubrfki0l68.cloudfront.net/3940247c12bffd3b66b4fec9b8ba7c196a053546/a3aba/img/blog/spark-books/3.png)](http://amzn.to/2ioCfPs)

This is a brand-new book (all but the last 2 chapters are available through early release), but it has proven itself to be a solid read.

Again written in part by Holden Karau, *High Performance Spark* focuses on data manipulation techniques using a range of spark libraries and technologies above and beyond core RDD manipulation. My gut is that if you’re designing more complex data flows as an engineer or data scientist then this book will be a great companion.

## [Spark in Action](http://amzn.to/2itnHkL)

[![Spark in Action](https://d33wubrfki0l68.cloudfront.net/050e4250615c38d2f5ad2418ce0c723ee1c94b8c/134af/img/blog/spark-books/spark-action.jpg)](http://amzn.to/2itnHkL)

*Spark in Action* tries to skip theory and get down to the nuts and bolts or doing stuff with Spark. The book will guide you through writing Spark Applications (with Python and Scala), understanding the APIs in depth, and spark app deployment options.

## [Pro Spark Streaming: The Zen of Real-Time Analytics Using Apache Spark](http://amzn.to/2jfQeve)

[![Pro Spark Streaming](https://d33wubrfki0l68.cloudfront.net/54f899abbac024b7a820916f31560ae099638eeb/ae702/img/blog/spark-books/5.png)](http://amzn.to/2jfQeve)

One of the key components of the Spark ecosystem is real time data processing.

As the only book in this list focused exclusively on real-time Spark use, this book will teach you how to deploy a Spark real-time data processing application from Scratch. It supports this with hands-on exercises and practical use-cases like on-line advertising, IoT, etc.

## [Mastering Apache Spark](http://amzn.to/2jFpqRZ)

[![Mastering Spark](https://d33wubrfki0l68.cloudfront.net/b744269809ef0d7b092dd81f5ef8dc390ce2052d/e150a/img/blog/spark-books/6.png)](http://amzn.to/2jFpqRZ)

Despite it’s title, this is truly a book for beginners. It covers a lot of Spark principles and techniques, with some examples. It includes a bunch of screen-shots and shell output, so you know what is going on. This book won’t actually make you a Spark master, but it is a good (and fairly short) way to get started.

## [Spark: Big Data Cluster Computing in Production](http://amzn.to/2ioQTGc)

[![Big Data Cluster Computing](https://d33wubrfki0l68.cloudfront.net/05e25edf58a4baf6341855f53532c388558779a7/9f646/img/blog/spark-books/7.png)](http://amzn.to/2ioQTGc)

If you are already a data engineer and want to learn more about production deployment for Spark apps, this book is a good start. You’ll learn how to monitor your Spark clusters, work with metrics, resource allocation, object serialization with Kryo, more. The book also discusses file format details (eg sequence files), and overall talks in a little more depth about app deployment than the average Spark book.

## [Learning Spark: Analytics With Spark Framework](http://amzn.to/2ioJ8jJ)

[![img](https://d33wubrfki0l68.cloudfront.net/e00ecdf2133c241d1672449a8f0a08741c627e58/05801/img/blog/spark-books/8.png)](http://amzn.to/2ioJ8jJ)

This book aims to be straight to the point: What is Spark? Who developed it? What are the use cases? What is the Spark-Shell? How to do Streaming with Spark? And how to work with Spark on EC2 and GCE?

This is a self published book so you might find that it lacks the polish of other books in this list, but it does go through the basics of Spark, and the price is right.

## [Spark Cookbook](http://amzn.to/2ilvBy5)

[![img](https://d33wubrfki0l68.cloudfront.net/5755f2fb0bceaa9681544ce3e27b14912fc483fb/d8b64/img/blog/spark-books/9.png)](http://amzn.to/2ilvBy5)

While *Spark Cookbook* does cover the basics of getting started with Spark it tries to focus on how to implement machine learning algorithms and graph processing applications. The book also tries to cover topics like monitoring and optimization. A good audience for this book would be existing data scientists or data engineers looking to start utilizing Spark for the first time.

## [Spark GraphX in Action](http://amzn.to/2ioEKRQ)

[![GraphX](https://d33wubrfki0l68.cloudfront.net/4d32452fe6c3dcea303d6bc365f12a5753c31c57/3eed0/img/blog/spark-books/10.png)](http://amzn.to/2ioEKRQ)

GraphX is a graph processing API for Spark. It tries to be both flexible and high-performance (much like Spark itself).

This is probably the most in-depth book on GraphX available (honestly it’s the only GraphX specific book available at the time of writing). *Spark GraphX in Action* starts with the basics of GraphX then moves on to practical examples of graph processing and machine learning. Overall I think it provides a great overview of the framework and a very practical jumping off point.

## [Big Data Analytics With Spark](http://amzn.to/2ioXyQL)

[![img](https://d33wubrfki0l68.cloudfront.net/856f066943722a38bbb9cd9f723a627878ac47aa/2d32c/img/blog/spark-books/11.png)](http://amzn.to/2ioXyQL)

This is another book for getting started with Spark, *Big Data Analytics* also tries to give an overview of other technologies that are commonly used alongside Spark (like Avro and Kafka).

It is full of great and useful examples (especially in the Spark SQL and Spark-Streaming chapters). Given the broad scope of the content in this book it maintains a fairly high level view of the ecosystem without going into too much depth. That said, it is yet another book that provides a great introduction to these technologies.

## Bonus Resources

Since Spark comes from a research laboratory in Berkeley University, the academic papers that originally described Spark are actually very useful. They allow you to dive deep into the Spark principles and understand exactly how things work under the hood. Also, each major Spark component usually has it’s own dedicated paper, which makes things even easier to break up.

A good place to start is with the paper `Resilient Distributed Datasets: A Fault-Tolerant Abstraction for In-Memory Cluster Computing`. If your brain can grok academic writing I even recommend reading it before you read one of the above books.

Here are some of the other available papers, each introducing a major Spark component.

1. Spark: Cluster Computing with Working Sets
2. Spark SQL: Relational Data Processing in Spark
3. MLib: Machine Learning in Apache Spark
4. GraphX: Unifying Data-Parallel and Graph-Parallel Analytics
5. Discretized Streams: An Efficient and Fault-Tolerant Model for Stream Processing on Large Clusters
6. SparkR: Scaling R Programs with Spark

All the papers can be downloaded for free at: [http://spark.apache.org/research.html)](http://spark.apache.org/research.html)

## Wrap Up

Hopefully these books can provide you with a good view into the Spark ecosystem. Learning a new technology is never easy, so if you have any other useful tips or tricks for your fellow learners feel free to add them to the comments section below.
