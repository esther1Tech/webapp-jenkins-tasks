pipeline {
    agent any
    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/esteem12/aws-jenkins-task.git'
            }
        }
        stage('Build') {
            steps {
                sh 'echo "Building the application"'
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Unit Test') {
            steps {
                sh 'echo "Running unit tests"'
                sh 'python3 -m unittest discover'
            }
        }
        stage('Deploy to Test Environment') {
            steps {
                sh 'echo "Deploying the application to the test environment"'
                sh 'nohup python3 app.py > /dev/null 2>&1 &'
            }
        }
    }
    post {
        success {
            echo 'CI/CD Pipeline completed successfully'
        }
        failure {
            echo 'CI/CD Pipeline failed'
        }
    }
}
