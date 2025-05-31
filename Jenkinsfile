pipeline {
    agent any

    stages {
        stage('With Docker') {
            steps {
                echo 'My Machine Node JS Vesrion'
                sh 'npm --version'
            }
        }
        stage('Without Docker') {
            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps {
                echo 'Node Version in Docker image'
                sh 'npm --version'
            }
        }
    }
}
