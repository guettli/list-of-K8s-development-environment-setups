# List of Kubernetes Development Environment Setups

I want to develop software which will run in Kubernetes later.

How to set up my local development environment?

There are thousand ways to do this, and I have no clue.

That's why I created this list. I want an overview of all options.

## Background: Hermetic Environment

I want my development environment to be **hermetic**. Which means
all services I need are on my local machine, or are mocked.
I want to be able to develop without internet connection.

For more about this topic you can read this [Hermetic Testing Article](https://testing.googleblog.com/2012/10/hermetic-servers.html).

## Background: IDE with GUI

Some freaks like to develop on machines with the text editor vi. This has the benefit that you can execute
it easily in a container. Although the start up phase feels fast, it is not not convenient and not efficient in the long run.

I want to use a modern IDE (for example an IntellJ based IDE or VSCode)

## Requirements

I need one or several services like: PostgreSQL, Nginx, Nodejs, ElasticSearch, Minio (S3), ....

How to get them running on my local machine?

I want a super fast edit/compile/test cycle (aka "inner loop"), since this gets done several hundret times per day.


## Option 1: Docker

The IDE need to support this.

TODO: Links to detailed docs.

## Option 2: Minikube

But how to get the code updates into the container? 

One solution: [Skaffold](https://skaffold.dev/)

Or [odo of OpenShift](https://github.com/openshift/odo)

## Option 3: local install

Install and run all services (DB, Cache, Webserver, ...) locally. Depending on your OS you have many choices (apt, snap, msi, ...). This could get automated with for example Ansible.


Pro:
* Accessing the services is easy. 

Con:
* Development environment and production environment are different.
  
  
I use this option now. I develop my Django code in a Python virtualenv. This is lightweight and easy. It does not matter if my code
runs in docker swarm, kubernetes or a VPS later.

