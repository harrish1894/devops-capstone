pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t sakthiemc123/devops-app .'
            }
        }

        stage('Push Docker Image') {
            steps {
                bat 'docker push sakthiemc123/devops-app'
            }
        }

    }
}