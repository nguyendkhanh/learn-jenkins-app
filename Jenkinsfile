pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps {
                echo 'Build Stage'
                sh '''
                ls -la
                node --version
                npm --version 
                npm ci
                npm build
                ls al
                '''
            }
        }
        stage('Test') {
            
            steps {
                echo 'This is the test stage'
                
            }
        }
    }
}
