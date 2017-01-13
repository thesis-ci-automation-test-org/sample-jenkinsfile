pipeline {
    agent any
    
    stages {
        stage('Prepare') {
            steps {
                echo 'Preparing' 
            }
        }
        
        stage('Test') {
            steps {
                parallel 'Smoke tests': {
                    sleep 15
                    echo 'Smoking'
                }, 'Unit tests': {
                    sleep 10
                    echo 'Uniting'
                }
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying stuff'
            }
        }
    }
}
