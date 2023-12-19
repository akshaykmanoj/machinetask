pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'GIT_key', url: 'https://github.com/akshaykmanoj/machinetask.git']])
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
    }
}
