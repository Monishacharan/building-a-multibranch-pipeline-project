pipeline {
    agent any
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
        stage('Deliver for development') {
            when {
                branch 'development' 
            }
            steps {
                sh '''
                    ls -lrt
                '''
            }
        }
        stage('Deploy for production') {
            when {
                branch 'production'  
            }
            steps {
                sh'''
                echo "successfull"
                '''
            }
        }
    }
}