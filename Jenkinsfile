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
        docker ps -q --filter "publish=5000" | xargs -r docker stop
        docker ps -aq --filter "publish=5000" | xargs -r docker rm
        docker run -d -p 5000:5000 --name mycontainer myapp
          '''
            }
        }
    }
}
