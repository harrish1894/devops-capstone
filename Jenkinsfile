pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t sakthiemc123/devops-app .'
            }
        }

        stage('Docker Login') {
            steps {
                bat 'docker login -u sakthiemc123 -p sowkiya@123'
            }
        }

        stage('Push Docker Image') {
            steps {
                bat 'docker push sakthiemc123/devops-app'
            }
        }

    }
}