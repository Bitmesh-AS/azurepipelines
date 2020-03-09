# Azure Build Pipelines Templates
Bitmesh AS is building services and applications where IoT has an esential role.
We build all our solutions as event driven microservices or just functions.

The services are hosted on Kubernetes in Azure.
This reposetory has a set of yml build files to make publishing services easier.

## Templates

1. Publish .net core web api service
2. Publish Angular App
3. Publish React.js App
4. Publish Nuget package

the deploy-* files are templates.
Use them as functions in your deployable project like in "myservice-deploy.yml".
All the build files relie on docker to build containers.

## Dev machin

Go to root. build with

docker-compose build --build-arg configuration="docker"

Add configuration for "docker". In angular app add in "environment.docker.ts". For react add ".env.local" for docker config.


