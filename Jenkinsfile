pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code'
            }
        }

        stage('Build') {
            steps {
                sh 'echo Building application'
            }
        }

        stage('Unit Test') {
            steps {
                sh 'echo Running tests'
            }
        }

        stage('Package') {
            steps {
                sh 'echo Packaging application'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t cheemslaika/astronomy-shop:v1 -f src/frontend/Dockerfile .'
            }
        }

        stage('Docker Push') {
            steps {

                withCredentials([usernamePassword(
                    credentialsId: 'dockerhub-credentials',
                    usernameVariable: 'DOCKER_USER',
                    passwordVariable: 'DOCKER_PASS'
                )]) {

                    sh '''
                    echo "$DOCKER_PASS" | docker login -u "$DOCKER_USER" --password-stdin

                    docker push cheemslaika/astronomy-shop:v1
                    '''
                }
            }
        }
    }
}
