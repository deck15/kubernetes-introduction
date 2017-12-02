Introduction to Kubernetes
==================

Links and resources used by the Introduction to Kubernetes DevOps Learning Journey course.

@Todo: Windows users: Please fill in the Windows installation prerequisites.

Table of Contents
-----------------
<!-- To generate Table of contents, do:
	npm update
	./node_modules/markdown-toc/cli.js --no-firsth1 README.md
-->
- [Notes](#notes)
- [Mac: Install Prerequisites](#mac-install-prerequisites)
- [Windows: Install Prerequisites](#windows-install-prerequisites)
- [Classroom](#classroom)
  * [What is Kubernetes](#what-is-kubernetes)
  * [Get Started: Local Kubernetes](#get-started-local-kubernetes)
  * [Azure Kubernetes Connect](#azure-kubernetes-connect)
  * [Kubernetes Connect](#kubernetes-connect)
  * [(Azure) Kubernetes Connect 101](#azure-kubernetes-connect-101)
  * [Go, gRPC and Kubernetes (Optional)](#go-grpc-and-kubernetes-optional)
  * [Kubernetes 101 (1st section)](#kubernetes-101-1st-section)
  * [Kubernetes 101 (2nd section)](#kubernetes-101-2nd-section)
  * [Kubernetes 101 (3rd section - Optional/extra credit)](#kubernetes-101-3rd-section---optionalextra-credit)
  * [Azure Kubernetes 201](#azure-kubernetes-201)
  * [Kubernetes Dashboard](#kubernetes-dashboard)
  * [Wordpress on Kubernetes](#wordpress-on-kubernetes)
  * [Elastic Search on K8s](#elastic-search-on-k8s)
  * [Kubernetes Stateful Application](#kubernetes-stateful-application)
  * [Kubernetes Configmap](#kubernetes-configmap)
  * [Kubernetes & Prometheus (Metrics)](#kubernetes--prometheus-metrics)
- [Additional Resources](#additional-resources)
  * [Reference Docs](#reference-docs)
  * [Kubernetes in Azure](#kubernetes-in-azure)
  
Notes
------------------
If you have VPN connected, you may encounter problems with your local docker connecting to a remote registry. Disconnect from VPN and then restart your terminal before continuing.

* **Mac** users should be able to download most tools and utilities using [brew](https://brew.sh/).
* **Windows** users may be able to download many tools and utilities using [Chocolatey](https://chocolatey.org/packages).

Mac: Install Prerequisites
------------------
1. Install Xcode from the [App Store](https://itunes.apple.com/us/app/xcode/id497799835?mt=12), or from [Apple Developer Downloads](https://developer.apple.com/xcode/downloads/)
2. [Install Homebrew](https://brew.sh/) using the following command:
    
	```sh
	/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
	```
    
3. Install Tools and Utilities:
	* [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/), [minikube](https://github.com/kubernetes/minikube), [Docker](https://docs.docker.com/docker-for-mac/install/), [VirtualBox](https://www.virtualbox.org/wiki/Downloads), [Docker Compose](https://docs.docker.com/compose/), [Docker Machine](https://docs.docker.com/machine/install-machine/), [Docker Machine driver xhyve](https://github.com/zchee/docker-machine-driver-xhyve), [Azure-CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest), and [NodeJS](https://nodejs.org/en/download/).

	```sh
	brew cask install docker
	brew cask install minikube
	brew cask install virtualbox
	brew install kubernetes-cli
	brew install docker-compose
	brew install docker-completion
	brew install docker-compose-completion
	brew install docker-machine-driver-xhyve
	brew install azure-cli
	brew install nodejs
	```

4. Set the preferences for the docker machine driver:

	```sh
	sudo chown root:wheel $(brew --prefix)/opt/docker-machine-driver-xhyve/bin/docker-machine-driver-xhyve
	sudo chmod u+s $(brew --prefix)/opt/docker-machine-driver-xhyve/bin/docker-machine-driver-xhyve
	```

Windows: Install Prerequisites
------------------
...

Classroom
---------

### What is Kubernetes

Introduction reading and video:

* [Illustrated Childrens Guide to Kubernetes](http://blog.kubernetes.io/2016/06/illustrated-childrens-guide-to-kubernetes.html)
* [Kubernetes - Getting Started](https://chrisshort.net/kubernetes-getting-started/)

### Get Started: Local Kubernetes

1. [Minikube Tutorial](https://kubernetes.io/docs/tutorials/stateless-application/hello-minikube/)
2. Install Hypervisor (Virtualbox, etc)
3. Stand up minikube and test

### Azure Kubernetes Connect

1. [Deploy an Azure Container Service (AKS) cluster](https://docs.microsoft.com/en-us/azure/aks/kubernetes-walkthrough) - _Will not currently work for connected cloud subscriptions._
2. Login to Azure
3. Download CLI and Login with CLI

### Kubernetes Connect

1. Create a cluster or use existing cluster created earlier.
2. Execute the [nginx example](https://github.com/kubernetes/kubernetes/blob/master/examples/simple-nginx.md).

### (Azure) Kubernetes Connect 101

1. [Tutorial: Prepare application for Azure Container Service (AKS)](https://docs.microsoft.com/en-us/azure/aks/tutorial-kubernetes-prepare-app)
2. [Tutorial: Deploy and use Azure Container Registry](https://docs.microsoft.com/en-us/azure/aks/tutorial-kubernetes-prepare-acr)
	* **Note:** If creating a registry in Azure is not possible, consider using your own public registry/repos in [Docker Hub](https://hub.docker.com/).
3. Create container images and run voting app locally. -- requires docker compose.
4. Upload voting app images to container registry created in step 2.

### Go, gRPC and Kubernetes (Optional)
* [Getting Started with Microservices using Go, gRPC and Kubernetes](https://outcrawl.com/getting-started-microservices-go-grpc-kubernetes/)
* [Source code for Getting Started with Microservices using Go, gRPC and Kubernetes](https://github.com/tinrab/kubernetes-go-grpc-tutorial)

1. Define Simple Services
	1. Comm protocol
	2. Common Divisor Services
	3. Frontend API Service
2. Build Docker Images
3. Deploy to K8s Cluster


### Kubernetes 101 (1st section)

1. [Kubernetes 101 Tutorial](https://github.com/gravitational/workshop/blob/master/k8s101.md)
2. Clone workshop Repo

	```sh
	git clone https://github.com/gravitational/workshop.git
	```
3. Classroom work: Running Nginx
	1. Standup Nginx
	2. Curl service from Tutum container
	3. Explore within the container
4. Follow sections:
	1. Running nginx
	2. Pod IPs
	3. Pod Containers

### Kubernetes 101 (2nd section)

1. [Kubernetes 101 Tutorial](https://github.com/gravitational/workshop/blob/master/k8s101.md)
2. Clone workshop Repo

	```sh
	git clone https://github.com/gravitational/workshop.git
	```
3. Classroom work sections:
	1. Deployments and Replicasets
	2. Services
	3. Back to Deployments
	4. Configuration management basics

### Kubernetes 101 (3rd section - Optional/extra credit)

1. [Kubernetes 101 Tutorial](https://github.com/gravitational/workshop/blob/master/k8s101.md)
2. Clone workshop Repo

	```sh
	git clone https://github.com/gravitational/workshop.git
	```
3. Sections: Connecting Services

**Note:** Requires a private registry locally or use of cloud registry, such as [Docker Hub](https://hub.docker.com/).

### Azure Kubernetes 201

1. Tutorials #3-5, Run and scale application exercises.
2. Tutorials 6 and 7 require [docker-compose](https://docs.docker.com/compose/install/).

* 3: [Deploy an Azure Container Service (AKS) cluster](https://docs.microsoft.com/en-us/azure/aks/tutorial-kubernetes-deploy-cluster)
* 4: [Run applications in Azure Container Service (AKS)](https://docs.microsoft.com/en-us/azure/aks/tutorial-kubernetes-deploy-application)
* 5: [Scale application in Azure Container Service (AKS)](https://docs.microsoft.com/en-us/azure/aks/tutorial-kubernetes-scale)
	* **Caution:** Scaling _nodes_ could come with some risk in the Class Azure subscription. Such as losing connection to your K8s master in your cluster. This happened to one engineer in DLJ#1 class. Cause unknown.
* 6: [Update an application in Azure Container Service (AKS)](https://docs.microsoft.com/en-us/azure/aks/tutorial-kubernetes-app-update)
* 7: [Monitor Azure Container Service (AKS)](https://docs.microsoft.com/en-us/azure/aks/tutorial-kubernetes-monitor)

### Kubernetes Dashboard

* [Tutorial: Azure AKS Kubernetes Dashboard](https://docs.microsoft.com/en-us/azure/aks/kubernetes-dashboard)

1. Tunnel to a local version of the kubernetes dashboard
2. Expose and edit two services within the kubernetes dashboard

### Wordpress on Kubernetes

* [Deploying WordPress and MySQL with Persistent Volumes](https://kubernetes.io/docs/tutorials/stateful-application/mysql-wordpress-persistent-volume/)

1. Create persistent volume
2. Create secret for MySQL password
3. Launch Wordpress

### Elastic Search on K8s

1. Clonse the examples repo
2. Deploy elasticsearch
3. Verify functionality

1. Clone [Kubernetes Examples repo](https://github.com/kubernetes/examples)

	```sh
	git clone git@github.com:kubernetes/examples.git
	```
2. Follow [Elastic Search Tutorial](https://github.com/kubernetes/examples/tree/master/staging/elasticsearch)

	Bonus:
3. [Deploy production ready cluster](https://github.com/pires/kubernetes-elasticsearch-cluster)
	```sh
	git clone git@github.com:pires/kubernetes-elasticsearch-cluster.git
	```
4. Bonus #2: Expose Kibana

### Kubernetes Stateful Application

1. Stand up and watch stateful mysql instances
	* [Run a Replicated Stateful Application](https://kubernetes.io/docs/tasks/run-application/run-replicated-stateful-application/)
2. Query and verify connectivity

### Kubernetes Configmap

1. Create Configmap
2. Consume Configmap in environment variables
3. Set command line using Configmap
4. Consume Configmap in Volume

* [ConfigMap Tutorial](http://pwittrock.github.io/docs/user-guide/configmap/)
* Use wget to get the files for the exercise...

	```sh
	wget http://pwittrock.github.io/docs/user-guide/configmap/configmap.yaml
	wget http://pwittrock.github.io/docs/user-guide/configmap/env-pod.yaml
	wget http://pwittrock.github.io/docs/user-guide/configmap/command-pod.yaml
	wget http://pwittrock.github.io/docs/user-guide/configmap/volume-pod.yaml
	wget http://pwittrock.github.io/docs/user-guide/configmap/mount-file-pod.yaml
	```
* Then apply using: (for example...)
	```sh
	kubectl create -f configmap.yaml
	```

### Kubernetes & Prometheus (Metrics)

* Follow [Tutorial: Collecting Metrics with Prometheus](https://github.com/kelseyhightower/oscon-2017-kubernetes-tutorial/blob/master/labs/06-tutorial-metrics.md)

1. Stand up [Prometheus](https://prometheus.io/docs/introduction/overview/)
2. Gather and monitor metrics


Additional Resources
------------------

### Reference Docs

* [Kubernetes by Example](http://kubernetesbyexample.com/) - A hands-on introduction to Kubernetes
* [kubectl Reference Cheat Sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)
* [Kubernetes Community Resources](http://k8s.info/index.html)
* [Kubernetes Community Resources - Cheat Sheet](http://k8s.info/cs.html)


### Kubernetes in Azure

* [Running Kubernetes in Azure](https://kubernetes.io/docs/getting-started-guides/azure/) - Basic information on options available.
* [Deploy a Kubernetes Cluster using ACS-Engine](https://github.com/Azure/acs-engine/blob/master/docs/kubernetes/deploy.md) - Getting started information.
* [Azure ACS-Engine Examples and Walkthroughs](https://github.com/Azure/acs-engine/tree/master/examples)

