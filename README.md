# Azure Build Pipelines Templates
This reposetory has a set of docker and kubernest files that make environment configuration seamless and easy.
On dev machin you can run the projects in docker with docker-compose.
On commit deployments are automaticaly deployed to correct environment based on branch.
Master is deployed to production and develop is published to test.

## Templates

1. deploy-service.yml Publish .net core web api service
2. deploy-ngapp.yml Publish Angular App
3. deploy-reactapp.yml Publish React.js App
4. deploy-nuget.yml Publish Nuget package

the deploy-* files are templates.
Use them as functions in your deployable project.
To se how they are used have a look at "myreactapp-deploy.yml", "myngapp-deploy.yml" and "myservice-deploy.yml"

## Dev machin

Go to root. build with

docker-compose build --build-arg configuration="docker"

In angular app add envinment speciffic config to "environment.docker.ts" for docker environment. For react add ".env.local" for docker environment.

## Bitmesh
Bitmesh AS is building services and applications for PropTech. With our own framework we focus on IoT centric application development.