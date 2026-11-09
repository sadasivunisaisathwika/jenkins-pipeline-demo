pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out source code...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building application...'
              bat '"C:\\Users\\SATHWIKA\\maven\\apache-maven-3.9.16\\bin\\mvn.cmd" clean compile'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                bat '"C:\\Users\\SATHWIKA\\maven\\apache-maven-3.9.16\\bin\\mvn.cmd" test'
            }
        }

        stage('Package') {
            steps {
                echo 
bat '"C:\\Users\\SATHWIKA\\maven\\apache-maven-3.9.16\\bin\\mvn.cmd" package'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}