pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building'
                sh 'docker build -t test/docker-react -f Dockerfile.dev .'
            }
        }
    }
}