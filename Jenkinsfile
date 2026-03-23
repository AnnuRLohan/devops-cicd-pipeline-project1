pipeline {
    agent any

    stages {

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
