pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'docker build -t api .'
            }
        }
        stage('Push to Docker Hub') {
            steps {
                sh 'docker login -u elias8477 -p vivesthomas'
                sh 'docker tag api elias8477/api:latest'
                sh 'docker push elias8477/api:latest'
            }
        }
    }
}