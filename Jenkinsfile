pipeline {
    agent any
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh '''
                    echo "This stage is built successfully"
                '''
            }
        }
        stage('Test') {
            steps {
                sh '''
                    echo "This stage is tested successfully"
                '''
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