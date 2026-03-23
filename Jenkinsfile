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
              docker stop mycontainer || true
        docker rm mycontainer || true
        docker run -d -p 5000:5000 --name mycontainer myapp
          '''
            }
        }
    }
}
