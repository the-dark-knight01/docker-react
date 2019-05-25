pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building'
                docker build -t test/docker-react -f Dockerfile.dev .
            }
        }
    }
}