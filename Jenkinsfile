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

        stage('Deploy') {
            steps {
                sh '''
                scp -i /var/lib/jenkins/.ssh/chai-key-pair.pem -o StrictHostKeyChecking=no -r hello-world.html ubuntu@54.152.14.241:/var/www/html/
                '''
            }
        }
    }
}

