pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh '''
                docker build -t lbg7-python-api .
                '''
            
            }
        }
        stage('Test') {
            steps {
                sh '''
                python lbg.test.py
                '''
            
            }
        }
        stage('Deploy') {
            steps {
                sh '''
                docker-compose down
                docker-compose up -d
                '''
                
            }
        }
    }
}