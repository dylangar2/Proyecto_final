pipeline {
    agent any

    stages {
        stage('Build Image') {
            steps {
                sh 'docker-compose build'
            }
        }

        stage('Push Image') {
            steps {
                sh 'docker push dylan226/proyecto2:ci'
            }
        }
    }
}
