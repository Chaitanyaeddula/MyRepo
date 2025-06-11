pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/your-user/your-repo.git'
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
                scp -i ~/.ssh/chai-key-pair.pem -r * ec2-user@<target-ec2-ip>:/var/www/html/
                '''
            }
        }
    }
}

