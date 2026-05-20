pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code'
            }
        }

        stage('Docker Build Frontend') {
            steps {
                sh 'docker build -t frontend:v1 -f src/frontend/Dockerfile .'
            }
        }
    }
}
