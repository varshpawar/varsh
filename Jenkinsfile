pipeline {

    agent {
        label 'docker'
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                url: 'https://github.com/varshpawar/varsh.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t varshpawar/food-app:latest .'
            }
        }

        stage('Push Docker Image') {
            steps {
                sh 'docker push varshpawar/food-app:latest'
            }
        }

    }
}
