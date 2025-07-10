pipeline {
    agent any

    stages {
        stage('Clone Code') {
            steps {
                git url: 'https://github.com/nnaredla1357/mytest.git', branch: 'main'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t myimage .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run --rm myimage'
            }
        }
    }
}
