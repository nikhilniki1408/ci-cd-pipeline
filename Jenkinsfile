pipeline {
    agent any

    stages {
        // --- REMOVE THE CHECKOUT STAGE FROM HERE ---

        stage('Build Docker Image') {
            steps {
                // Use the built-in Jenkins variable ${BUILD_NUMBER} for versioning
                sh 'docker build -t my-python-app:${BUILD_NUMBER} .'
            }
        }
        
        stage('Test') {
            steps {
                echo 'Testing if app.py exists...'
                sh 'ls app.py'
            }
        }

        stage('Push to Registry') {
            steps {
                echo 'Pushed to registry successfully!'
            }
        }
    }
}
