[![manu-paul](https://circleci.com/gh/manu-paul/project-ml-microservice-kubernetes.svg?style=svg)](https://circleci.com/gh/manu-paul/project-ml-microservice-kubernetes)

<b>How to Run Python script?</b><br>

Python3 -m venv ~/.devops<br>
make install<br>
python3 app.py<br><br>

<b>What is the repository files?</b>

.circleci/config.yml -  script that build the project on cilcleci<br>
model_data directory has python module that will be imported in the code<br>
Output_txt_files directory that includes the output log of docker containers and the cluster pod logs<br>
app.py - python code file<br>
Dockerfile - core file to generate docker image<br>
make_prediction.sh - script to test the python application<br>
requirments.txt - is the file that has the needed python libraries<br>
run_docker.sh - script that create an image and run container<br>
upload_docker.sh - script that push the docker image to dockerhub<br>
run_kubernetes.sh - script that create kubernetes cluster and run the app on mapped port<br>
