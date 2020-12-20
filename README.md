[![manu-paul](https://circleci.com/gh/manu-paul/project-ml-microservice-kubernetes.svg?style=svg)](https://circleci.com/gh/manu-paul/project-ml-microservice-kubernetes)

How to Run Python script?

Python3 -m venv ~/.devops
make install
python3 app.py
What is the repository files?

.circleci directory has config.yml file that will build the project on cilcleci
model_data directory has python module that will be imported in the code
Output_txt_files directory that includes the output log of docker containers and the cluster pod logs
app.py is the python code file
Dockerfile is the core file to generate docker image
make_prediction.sh script to test the python application
requirments.txt is the file that has the needed python libraries
run_docker.sh script that create an image and run container
upload_docker.sh script that push the docker image to dockerhub
run_kubernetes.sh script that create kubernetes cluster and run the app on mapped port
