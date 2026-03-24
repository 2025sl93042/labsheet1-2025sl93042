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
        sshagent(['aws-key']) {
            sh '''
            scp -o StrictHostKeyChecking=no \
            calculator.py \
            ec2-user@13.61.26.104:/home/ec2-user/
            '''
        }
    }
}

    }
}
