pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t sakthiomc123/devops-app .'
            }
        }

        stage('Push Docker Image') {
            steps {
                bat 'docker push sakthiomc123/devops-app'
            }
        }

    }
}