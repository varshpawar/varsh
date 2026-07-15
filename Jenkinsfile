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
                sh 'docker build -t food-app .'
            }
        }

    }
}
