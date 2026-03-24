pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'python3 --version'
                sh 'ls -l'
            }
        }

        stage('Test') {
            steps {
                sh 'python3 test_calculator.py'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploy stage placeholder"
            }
        }

    }
}
