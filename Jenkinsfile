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
                echo 'This is Build Stage'
                sh '''
                ls -la
                node --version
                npm --version 
                npm i
                npm build
                ls -al
                '''
            }
        }
        stage('Test') {
            
            steps {
                echo 'This is the Test Stage'
                
            }
        }
    }
}
