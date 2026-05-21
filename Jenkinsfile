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
                sh 'docker build -t astronomy-shop:v1 -f src/frontend/Dockerfile .'
            }
        }
    }
}
