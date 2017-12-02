Introduction to Kubernetes
==================

Links and resources used by the Introduction to Kubernetes DevOps Learning Journey course.

@Todo: Windows users: Please fill in the Windows installation prerequisites.

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
4. View [Kubernetes Dashboard](https://docs.microsoft.com/en-us/azure/aks/kubernetes-dashboard)

### Kubernetes Connect

1. Create a cluster or use existing cluster created earlier.
2. Execute the [nginx example](https://github.com/kubernetes/kubernetes/blob/master/examples/simple-nginx.md).

### (Azure) Kubernetes Connect 101

1. [Tutorial: Prepare application for Azure Container Service (AKS)](https://docs.microsoft.com/en-us/azure/aks/tutorial-kubernetes-prepare-app)
2. [Tutorial: Deploy and use Azure Container Registry](https://docs.microsoft.com/en-us/azure/aks/tutorial-kubernetes-prepare-acr)
	* **Note:** If creating a registry in Azure is not possible, consider using your own public registry/repos in [Docker Cloud](https://cloud.docker.com).
3. Create container images and run voting app locally. -- requires docker compose.
4. Upload voting app images to container registry created in step 2.

Additional Resources
------------------

### Reference Docs

* [Kubernetes by Example](http://kubernetesbyexample.com/) - A hands-on introduction to Kubernetes
* [kubectl Reference Cheat Sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)
* [Kubernetes Community Resources](http://k8s.info/index.html)
* [Kubernetes Community Resources - Cheat Sheet](http://k8s.info/cs.html)
* [Configure containers using a ConfigMap](https://kubernetes.io/docs/tasks/configure-pod-container/configmap/)
* [ConfigMap Example](http://pwittrock.github.io/docs/user-guide/configmap/)

### Walkthroughs and Tutorials

* [Kubernetes 101 Workshop](https://github.com/gravitational/workshop/blob/master/k8s101.md) - Introduction to Kubernetes and basic concepts
* [Deploying WordPress and MySQL with Persistent Volumes](https://kubernetes.io/docs/tutorials/stateful-application/mysql-wordpress-persistent-volume/)
* [Collecting Metrics with Prometheus](https://github.com/kelseyhightower/oscon-2017-kubernetes-tutorial/blob/master/labs/06-tutorial-metrics.md)

### Kubernetes in Azure

* [Running Kubernetes in Azure](https://kubernetes.io/docs/getting-started-guides/azure/) - Basic information on options available.
* [Deploy a Kubernetes Cluster using ACS-Engine](https://github.com/Azure/acs-engine/blob/master/docs/kubernetes/deploy.md) - Getting started information.
* [Azure ACS-Engine Examples and Walkthroughs](https://github.com/Azure/acs-engine/tree/master/examples)


