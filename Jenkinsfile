pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t sakthiomc123/devops-app .'
            }
        }

        stage('Push Docker Image') {
            steps {
                sh 'docker push sakthiomc123/devops-app'
            }
        }

    }
}