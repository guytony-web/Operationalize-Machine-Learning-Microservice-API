

[![CircleCI](https://dl.circleci.com/status-badge/img/gh/guytony-web/projectguy4/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/guytony-web/projectguy4/tree/main)
# Operationalize a Machine Learning Microservice API
## Project Overview

This is a repository for the fourth project in the AWS Cloud DevOps Engineer Udacity Nanodegree.
You are given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

The project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project you will:
* Test your project code using linting
* Complete a Dockerfile to containerize this application
* Deploy your containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that your code has been tested

---

## Setup the Environment

* Create a virtualenv with Python 3.7 and activate it(You should have Python 3.7 available in your host)

python3 -m venv ~/.devops
source ~/.devops/bin/activate

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


### Project Files

* __.circleci/config.yml:__ CircleCI configuration file.
* __hadolint:__ Hadolint v1.17.5 Linux-86_64 executable. 
* __app.py:__ The Flask web application
* __model_data/boston_housing_prediction.joblib:__ Pretrained sklearn model
* __requirements.txt:__ Required Python packages to run the application
* __Makefile:__ Commands to install and lint the application
* __Dockerfile:__ Defines the Docker container to run the application in
* __upload_docker.sh:__ Tags and uploads the Docker image to DockerHub
* __run_docker.sh:__ Runs the application in a Docker container (defined by the Dockerfile)
* __run_kubernetes.sh:__ Runs the application on a Kubernetes cluster
* __make_prediction.sh:__ Makes a prediction call to the running Application on port 8000
* __output_txt_files/docker_out.txt:__ Console output from running run_docker.sh and make_prediction.sh
* __output_txt_files/kubernetes_out.txt__ Console output from running run_kubernetes.sh and make_prediction.sh
