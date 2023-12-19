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
                script {
                    sh 'npm install'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    sh 'cp index.html /var/www/html/'
                }
            }
        }

        stage('Capture Screenshot') {
            steps {
                script {
                    sh 'npm install puppeteer'
                    sh 'node capture-screenshot.js'
                    sh 'mv screenshot.png ~/screenshot.png'
                }
            }
        }
    }
}
