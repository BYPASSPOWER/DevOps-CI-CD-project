pipeline {
    agent any

    environment {
        IMAGE_NAME = "devops-node-app"
    }

    stages {
        stage('Build Docker Image') {
            steps {
                dir('app') {
                    sh 'docker build -t $IMAGE_NAME .'
                }
            }
        }

        stage('Load Image to KIND') {
            steps {
                sh 'kind load docker-image $IMAGE_NAME'
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                sh 'kubectl apply -f k8s/'
            }
        }
    }
}




