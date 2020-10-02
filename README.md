# List of Kubernetes Development Environment Setups

I want to develop software which will run in Kubernetes later.

How to set up my local development environment?

There are thousand ways to do this, and I have no clue.

That's why I created this list.

## Hermetic

I want my development environment to be **hermetic**. Which means
all services I need are on my local machine, or are mocked.
I want to be able to develop without internet connection.

For more about this topic you can read this [Hermetic Testing Article](https://testing.googleblog.com/2012/10/hermetic-servers.html).

## Docker vs minikube vs local install

I need one or several services like: PostgreSQL, Nginx, Nodejs, ElasticSearch, Minio (S3), ....

How to get them running on my local machine?

I see these ways:

* install them locally. Depending on your OS you have many choices (apt, snap, msi, ...). This could get automated with for example Ansible.
* use docker
* use minikube


