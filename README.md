# CI/CD Pipeline for Web Application Using Jenkins

This repository contains the source code and configuration for setting up a CI/CD pipeline for a web application using Jenkins and Git.

## Application Overview

The web application is a Flask application that includes two templates:
- `index.html`: Contains a form to enter a name.
- `greet.html`: Displays a greeting message with the entered name.

## Setup

1. **GitHub Repository**: Create a GitHub repository for the web application.
2. **Jenkins Server**: Set up a Jenkins server and connect it to the GitHub repository using Webhook.
3. **Configure Jenkins Pipeline**: The Jenkins pipeline is added to do the deployment on every push to repo
4. **Test Environment**: AWS EC2 server is used as test environment, where the application gets deployed for testing. 

## CI/CD Pipeline Stages

- **Git Checkout**: Checkout the code from the GitHub repository.
- **Build**: Build the application by installing dependencies listed in `requirements.txt`.
- **Unit Test**: Run unit tests for the application.
- **Deploy to Test Environment**: Deploy the application to the test environment.

## How to Run the CI/CD Pipeline

1. Push changes to the GitHub repository.
2. Jenkins will automatically trigger the pipeline.
3. Monitor the pipeline status in Jenkins.
4. Access the deployed application in the test environment to verify functionality.


**Jenkins URL** [http://3.14.82.119:8080/](http://3.14.82.119:8080/)
**Application URL** [http://3.14.82.119:5000/](http://3.14.82.119:5000/)
