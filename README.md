[![CircleCI](https://circleci.com/gh/richardhowes/operationalise-ml-microservice-api.svg?style=svg)](https://circleci.com/gh/richardhowes/operationalise-ml-microservice-api)

## Project Overview

In this project, you will apply the skills you have acquired in this course to operationalize a Machine Learning Microservice API. 

You are given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

Your project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project you will:
* Test your project code using linting
* Complete a Dockerfile to containerize this application
* Deploy your containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that your code has been tested

You can find a detailed [project rubric, here](https://review.udacity.com/#!/rubrics/2576/view).

**The final implementation of the project will showcase your abilities to operationalize production microservices.**

---

## Setup the Environment

* Create a virtualenv and activate it
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`
4. Run a prediction: `./make_prediction.sh` 

Point 4 confirms the system is working and should have output simlar to this: 
```Port: 8000
{
  "prediction": [
    20.35373177134412
  ]
}
``` 

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl

### Project Files

1. `Dockerfile` : builds the docker image.

2. `app.py` : The the simple test flask app

3. `make_prediction.sh` : runs a query against the machine learning API.

4. `requirements.txt` : python application dependencies.

5. `run_docker.sh` : builds and runs the docker image.

6. `upload_docker.sh`: upload the docker image to the docker hub.

7. `run_kubernetes.sh` : downloads the docker image from the docker hub and run this image locally on a kubernetes cluster.

8. `model_data` : machine learning data prerequisites.

9. `./output_txt_files` : the output from `run_docker.sh`: docker_out.txt, and `run_kubernetes.sh`: kubernetes_out.txt.