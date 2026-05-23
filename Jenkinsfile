pipeline {
    agent any

    environment {
        PATH = "C:\\Program Files\\nodejs\\;${env.PATH}"
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Test Node') {
            steps {
                bat 'node -v'
                bat 'npm -v'
            }
        }

        stage('Run') {
            steps {
                bat 'npm start'
            }
        }
    }
}