pipeline {
    agent any
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building'
                sh 'docker build -t test/docker-react -f Dockerfile.dev .'
            }
        }
    }
    stages {
        stage('Test') {
            steps {
                echo 'Testing'
                sh 'docker run test/docker-react npm run test -- --coverage'
            }
        }
    }   
}