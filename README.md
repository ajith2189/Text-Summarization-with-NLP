# Text-Summarization-with-NLP


![Firefly 20241120152724](https://github.com/user-attachments/assets/b0735424-a3da-4821-8278-03be6561fb5f)

The Text Summarization NLP Project is a comprehensive machine learning application focused on automating text summarization using Natural Language Processing. Key features include:

Objective: Develop an automated text summarization system

    Technology Stack: Python, NLP libraries, Docker, AWS

Components:

    Data processing and model development
    API creation for user interaction
    Docker containerization
    AWS cloud deployment

Project Structure:

    Modular design with configuration management
    GitHub Actions for CI/CD

Development Workflow:

    Entity creation, component development, and pipeline integration
    Main application in main.py and app.py

Deployment:

    Docker containerization
    AWS services (ECR, EC2) for hosting
    GitHub Actions for automated deployment

Setup and Execution:

    Conda for environment management
    Local and cloud deployment instructions

This project showcases best practices in NLP application development, cloud deployment, and DevOps, making it valuable for data scientists and ML engineers looking to understand the full lifecycle of deploying NLP models in a production environment.

## Workflows

1. Update config.yaml
2. Update params.yaml
3. Update entity
4. Update the configuration manager in src config
5. update the conponents
6. update the pipeline
7. update the main.py
8. update the app.py



# How to run?
### STEPS:

    Clone the repository

```bash
https://github.com/entbappy/End-to-end-Text-Summarization
```
### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n summary python=3.8 -y
```

```bash
conda activate summary
```


### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```


```bash
# Finally run the following command
python app.py
```

Now,
```bash
open up you local host and port
```


```bash
Author: Ajith C
AI/ML Engineeer
Email: ajith218907@gmail.com

```



# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

	#with specific access

	1. EC2 access : It is virtual machine

	2. ECR: Elastic Container registry to save your docker image in aws


	#Description: About the deployment

	1. Build docker image of the source code

	2. Push your docker image to ECR

	3. Launch Your EC2 

	4. Pull Your image from ECR in EC2

	5. Lauch your docker image in EC2

	#Policy:

	1. AmazonEC2ContainerRegistryFullAccess

	2. AmazonEC2FullAccess

	
## 3. Create ECR repo to store/save docker image
    - Save the URI: 566373416292.dkr.ecr.us-east-1.amazonaws.com/text-s

	
## 4. Create EC2 machine (Ubuntu) 

## 5. Open EC2 and Install docker in EC2 Machine:
	
	
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
# 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets:

    AWS_ACCESS_KEY_ID=

    AWS_SECRET_ACCESS_KEY=

    AWS_REGION = us-east-1

    AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com

    ECR_REPOSITORY_NAME = simple-app


