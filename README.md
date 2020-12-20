[![manu-paul](https://circleci.com/gh/manu-paul/project-ml-microservice-kubernetes.svg?style=svg)](https://circleci.com/gh/manu-paul/project-ml-microservice-kubernetes)

## Project Overview
This project is to operationalize a Python based Machine Learning Microservice API. 

## How to Run Python script?

* Python3 -m venv ~/.devops
* make install
* python3 app.py

## Setup the Environment

* Create a virtualenv and activate it
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

## What are the repository files?

* .circleci/config.yml -  script that build the project on cilcleci
* model_data directory has python module that will be imported in the code
* Output_txt_files directory that includes the output log of docker containers and the cluster pod logs
* app.py - python code file
* Dockerfile - core file to generate docker image
* make_prediction.sh - script to test the python application
* requirments.txt - is the file that has the needed python libraries
* run_docker.sh - script that create an image and run container
* upload_docker.sh - script that push the docker image to dockerhub
* run_kubernetes.sh - script that create kubernetes cluster and run the app on mapped port

### Project Tasks

* Test your project code using linting
* Complete a Dockerfile to containerize this application
* Deploy your containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that your code has been tested



### Kubernetes Steps

* minikube installation<br>
brew install minikube

* Start a cluster using the docker driver:<br>
minikube config set driver docker<br>
minikube start --driver=docker<br>

* Deploy and Application in Kubernetes<br>
./run_kubernetes.s

