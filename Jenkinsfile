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
    }
}

