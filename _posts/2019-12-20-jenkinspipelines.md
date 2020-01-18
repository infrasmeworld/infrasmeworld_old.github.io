---
title: "Jenkins — Pipeline"
date: 2019-12-20
tags: [jenkins, devops]
header:
  image: "/images/cloud.png"
excerpt: "Jenkins, devops, pipelines"
---

## Jenkins:

Jenkins is an open source automation server written in Java. Jenkins helps to automate the non human part of the software development cycle with continuous integration and continuous delivery. 

It is a server-based system that run on servlet containers such as apache tomcat. 

## Jenkins Pipeline:

Jenkins pipeline is a set of plugins which supports implementing and integrating continuous delivery pipelines into Jenkins.

## CD Pipeline:

Continuous delivery pipeline is the automated process of getting your software from version controlled code repository to your end users. Each committed change to the software code will go through a series of defined steps before getting released. This involves building the software and then going through different tests and deployments.

## Jenkins File:

Jenkins file keeps the list of jobs which the pipeline will perform. It can be held in Jenkins server itself as part of the pipeline or in a Git repo. Jenkinsfile can be written in two syntax, Declarative and Scripted.


## Example Jenkins file:

Jenkinsfile (Declarative Pipeline)

```

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}

```