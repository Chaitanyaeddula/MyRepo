pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'echo Build completed'
            }
        }

        stage('Test') {
            steps {
                sh 'echo Running tests'
            }
        }

        stage('Run remote commands') {
            steps {
                sh '''
                   ssh -i /var/lib/jenkins/.ssh/chai-key-pair.pem -o StrictHostKeyChecking=no ubuntu@54.152.14.241 "echo Hello from EC2; hostname; uptime"
                '''
            }
        }
    }
}

