pipeline {
    agent any

    stages {

        stage('Clone Repo') {
            steps {
                git 'https://github.com/harrrish1894/devops-capstone.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t sakthi0mc123/devops-app .'
            }
        }

        stage('Push Docker Image') {
            steps {
                sh 'docker push sakthi0mc123/devops-app'
            }
        }

    }
}