pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/YOUR_USERNAME/devops-cicd-pipeline-project1.git'
            }
        }

        stage('Build') {
            steps {
                sh 'echo "Building Docker image..."'
            }
        }

        stage('Test') {
            steps {
                sh 'echo "Running tests..."'
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "Deploying app..."'
            }
        }
    }
}
