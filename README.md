# Docker_Kubernetes
It's a project number 4 for Cloud DevOps Engineer Nanodegree  I got an app and i tested it using linting and i made Dockerfile for it and deployed it using Kubernetes with CI/CD using CircleCI.

## requirements.txt
It contains the required packages for the app.

## Makefile
We use this file in local to setup virtual environment in python3 and test the docker file and python file using lint.
```sh
$ make install
$ make lint
```

## Dockerfile
The used file for building the docker. it uses python3.7.3-stretch then copy app.py to different directory then install the required packages for the project and the needed port(port 80).

## run_docker.sh
It builds the docker file with tag=api then lists all images and run the docker file in port 8000 instead of 80.
```sh
$ ./run_docker.sh
```

## make_prediction.sh
It contain case for testing in production using localhost:port. It POSTs a request then get a reply in json file.
```sh
$ ./make_prediction.sh
```

## upload_docker.sh
It pushs the docker image to my docker hub account.
```sh
$ ./upload_docker.sh
```

## run_kubernetes.sh
It runs the docker image from my repo on docker hub on kubernetes on port 80 then forward the port to 8000 instead of 80. 
```sh
$ ./run_kubernetes.sh
```

## CircleCI State
[![AymanAzzam](https://circleci.com/gh/AymanAzzam/Docker_Kubernetes.svg?style=svg)](https://app.circleci.com/pipelines/github/AymanAzzam/Docker_Kubernetes)
