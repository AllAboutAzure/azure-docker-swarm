# Deploy .Net web application in Azure vm - with Docker Swarm Architecture

**Note:** This repository contains code which can act a template in build and deploying the application in Azure set up as discussed with the architecture in my blog \
**Reference:** 

**Pipelines**
1. application-build: containerzise the .Net MVC application and publish it in Azure COntainer registry
2. application-deploy: pull the image from azure container registry and publish the service in self hosted docker swarm enabled (installed) vm.

This two pipelines act as templates;\
**Alernatively**: 
1. you can build and publish the dockerized image directly into the self hosted vm. instead of of pushing and pull
2. another alertive is push the image to ACR, publish the artifact, then in the same pipeline / workflow - you can create a succession job and download the artificat and you can publish the image into the vm.
