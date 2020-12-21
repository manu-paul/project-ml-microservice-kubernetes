[![manu-paul](https://circleci.com/gh/manu-paul/project-ml-microservice-kubernetes.svg?style=svg)](https://circleci.com/gh/manu-paul/project-ml-microservice-kubernetes)

## Project Overview
This project is to operationalize a Python based Machine Learning Microservice API. 


## Setup the Environment
* Create a virtualenv and activate it
python3 -m venv ~/.devops <br>
source ~/.devops/bin/activate
* Run `make install` to install the necessary dependencies
* Run `make lint` to lint checks on the project code

### Running `app.py`
1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

## What are the repository files?
* Makefile - Contains the list of project dependencies to be installed
* requirments.txt - Contains the required python libraries for the make step above
* .circleci/config.yml -  script that build the project on cilcleci
* model_data directory - has the python module that will be imported in the code
* output_txt_files - directory that includes the output of docker container and the kubenetes cluster pod logs
* app.py - python code file
* Dockerfile - core file to generate docker image
* make_prediction.sh - script to test the python application
* run_docker.sh - script that create an image and run container
* upload_docker.sh - script that push the docker image to dockerhub
* run_kubernetes.sh - script that create kubernetes cluster and run the app on mapped port
* output_txt_files/kubernetes_terminal.png - Shows the terminal output of kubernetes run

### Kubernetes Steps
* minikube installation<br>
brew install minikube

* Start a cluster using the docker driver:<br>
minikube config set driver docker<br>
minikube start --driver=docker<br>

* Deploy and Application in Kubernetes<br>
./run_kubernetes.s
