pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/Chaitanyaeddula/MyRepo.git'
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
                scp -i ~/.ssh/chai-key-pair.pem -r * ec2-user@54.152.14.241:/var/www/html/
                '''
            }
        }
    }
}

