---
title: Create Camel
linktitle: Create Camel
description: How to create a new Apache Camel microservice and import it into Jenkins X
date: 2017-02-01
publishdate: 2017-02-01
lastmod: 2017-02-01
menu:
  docs:
    parent: "developing"
    weight: 46
weight: 46
sections_weight: 46
categories: [fundamentals]
draft: false
toc: true
---

If you want to create a new Spring Boot based microservice using [Apache Camel](http://camel.apache.org/) you can use the [jx create camel](/commands/jx_create_camel) command.


```shell
$ jx create camel
```

You are then prompted for the project name.

If you want you can specify this on the command line:

```shell
$ jx create camel -a myapp
```


### What happens when you create a camel microservice

Once you have chosen the project to create and given it a name the following is automated for you:

* creates a new camel microservice in a sub directory
* add your source code into a git repository 
* create a remote git repository on a git service, such as [GitHub](https://github.com)
* push your code to the remote git service
* adds default files:
  * `Dockerfile` to build your application as a docker image
  * `Jenkinsfile` to implement the CI / CD pipeline
  * helm chart to run your application inside Kubernetes
* register a webhook on the remote git repository to your teams Jenkins
* add the git repository to your teams Jenkins
* trigger the first pipeline 
