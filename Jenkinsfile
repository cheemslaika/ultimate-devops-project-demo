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
                sh 'echo Running unit tests'
            }
        }

        stage('Package') {
            steps {
                sh 'echo Packaging application'
            }
        }
    }
}
