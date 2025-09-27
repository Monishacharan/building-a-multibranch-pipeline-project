pipeline {
    agent any
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh '''
                    echo "This stage is built successfully in production"
                '''
            }
        }
        stage('Test') {
            steps {
                sh '''
                    echo "This stage is tested successfully in production"
                '''
            }
        }
        stage('development') {
            when {
                branch 'development' 
            }
            steps {
                sh '''
                    ls -lrt
                '''
            }
        }
        stage('production') {
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