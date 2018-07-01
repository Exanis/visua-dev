# visua-dev
Dev tooling for Visua

## What is this ?

Visua is a simple tool aiming to non-programmers to let them process and manage vast amount of data. It is splitted in three parts: a runner, an API and a frontend. This project is a set of tooling (mostly skaffold / kubernetes configuration) used to help testing / deploying it. Documentation, as well as backlog and bug reporting, can be found in the main project [here](https://github.com/Exanis/visua)

## How to run those tools

Visua tools assume that you will have a way to deploy to a kubernetes (minikube works fine) with an usable ingress. To add it on minikube, just run :

`minikube addons enable ingress`

Visua then use skaffold to manage and rebuild images. It will assume that your folders looks like this:

```my-folder/
    visua-api/
    visua-dev/
```

If you need to change this, just edit `skaffold.yaml`.

## Important warning

Those tools are not mean for production use. There is no HA, no persistance, nothing like that. They are to create an easy way to develop on your local computer.