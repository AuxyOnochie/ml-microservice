
[![CircleCI](https://dl.circleci.com/status-badge/img/gh/AuxyOnochie/ml-microservice/tree/master.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/AuxyOnochie/ml-microservice/tree/master)
## Project Overview

As a DevOps professional, this project tests my ability to work with a data science team that has built a Flask application that takes payload to predicts housing prices in Botson. I containerized using Docker and Kubernetes, making it a completely scalable machine learning service that is available via Flask API.

### Project Steps

The project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project you will:
* Test my project code using linting `make lint`
* Complete a Dockerfile to containerize this application
* Deploy your containerized application using Docker and make a prediction `run_docker.sh` and `make_prediction.sh`
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster `minikube start`
* Deploy a container using Kubernetes and make a prediction  `run_kubernetes.sh`
* Upload a complete Github repo with CircleCI to indicate that your code has been tested

You can find a detailed [project rubric, here](https://review.udacity.com/#!/rubrics/2576/view).

## Requirements
 - Python 3.7

---
### Explanation of files
1. circleci/config.yml ---- circleci configuration
2. Dockerfile ---- Docker configuration file
3. make_prediction.sh ---- A script for  logging  predictions endpoint output
4. Makefile ---- This contains instructions on environment setup,dependencies installation instruction, and lint tests
5. requirements.txt ---- This contains python dependencies for the project
6. run_docker.sh ---- A shell script to build docker image and run it
7. model_data ---- contains housing prices in Boston area
8. output_txt_files/docker_out.txt ---- contains docker log outputs
9. output_txt_files/kubernetes_out.txt ---- contains kubernetes log outputs
10. app.py - flask app API endpoint with routes to get house prices in Boston
11. run_kubernetes.sh ----- A  shell script for  running   Docker Hub container with kubernetes
12. upload_docker.sh ---- A  shell script for  uploading local docker build image to docker hub that is online.
 



## Setup the Environment

* Create a virtualenv with Python 3.7 and activate it. Refer to this link for help on specifying the Python version in the virtualenv. 
```bash
python3 -m pip install --user virtualenv
# You should have Python 3.7 available in your host. 
# Check the Python path using `which python3`
# Use a command similar to this one:
python3 -m virtualenv --python=<path-to-Python3.7> .devops
source .devops/bin/activate
```
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl
