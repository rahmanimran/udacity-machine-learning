[![rahmanimran](https://circleci.com/gh/rahmanimran/udacity-machine-learning.svg?style=svg)](https://circleci.com/gh/rahmanimran/udacity-machine-learning)

**Git Repo:** https://github.com/rahmanimran/udacity-machine-learning

## STEPS:

1. Create a virtualenv and activate it.
	- python3 -m venv ~/.devops
	- source ~/.devops/bin/activate   

2. Install necessary dependencies with Makefile
	- make install

3. Check the python app first. It should be working.
	- python3 app.py

4. Run the Python app in Docker
	- chmod +x run_docker.sh
	- ./run_docker.sh
	
5. Make prediction from a separate window
	- ./make_prediction.sh

6. Run the app in Kubernetes
	- chmod +x run_kubernetes.sh
	- ./run_kubernetes.sh

7. Make prediction:
	- chmod +x make_prediction_k8s.sh
	- ./make_prediction_k8s.sh
	
8. Adding Circle CI
	- Open an account in Circle CI and include the github project.


## FILES:

**makefile**
	Setup instruction of python environment and lint.

**app.py**
	Python code which we will run.

**Dockerfile**
	Definition of the Docker container which will expose the service in port 80.

**run_docker.sh**
	Building docker container from Docker file and run it on port 8000

**make_prediction.sh**
	Tests the docker container connecting with port 8000

**upload_docker.sh**
	Uploads the image to dockerhub

**run_kubernates.sh**
	Pulls the docker image and creates deployment.

**make_prediction_k8s.sh**
	Tests kubernetes cluster connecting with port 8001

**docker_out.txt**
	Output of terminal while running docker

**kubernetes_out.txt**
	Output of terminal while running kubernetes

**.circleci/config.yml**
	Circle Ci configuration mentioning steps to lint and build the project

## DEPENDENCIES:
1. I've done the project in AWS EC2. Used Amazin Linux 2.
2. Docker
3. Python3
4. pip3
5. Linuxbrew for simplified installation
6. Kubectl
7. Minikube
