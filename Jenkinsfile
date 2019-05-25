pipeline {

    agent any
    tools {
        docker 'docker-1.0'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building'
                // docker build -t test/docker-react -f Dockerfile.dev .
            }
        }stage('Test') {
            steps {
                echo 'Testing'

                // docker run test/docker-react npm run test -- --coverage
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }
    }

    post {
        always {
            junit 'build/reports/**/*.xml'
        }
    }
    post {
        always {
            echo 'One way or another, I have finished'
            deleteDir() /* clean up our workspace */
        }
        success {
            echo 'I succeeeded!'
        }
        unstable {
            echo 'I am unstable :/'
        }
        failure {
            echo 'I failed :('
        }
        changed {
            echo 'Things were different before...'
        }
    }
}