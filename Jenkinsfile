pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/akshaykmanoj/machinetask.git'
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
