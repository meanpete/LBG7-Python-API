pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh '''
                docker build -t lbg7-python-api .
                '''
                //
            }
        }
        stage('Test') {
            steps {
                sh '''
                python lbg.test.python
                '''
                //
            }
        }
        stage('Deploy') {
            steps {
                Sh '''
                docker compose up -d
                //
            }
        }
    }
}