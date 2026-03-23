pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t myapp .'
            }
        }

        stage('Run Container') {
            steps {
                sh '''
              docker stop intelligent_meitner || true
        docker rm intelligent_meitner || true
        docker run -d -p 5000:5000 --name mycontainer myapp
          '''
            }
        }
    }
}
