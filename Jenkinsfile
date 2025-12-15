pipeline {
    agent any

    stages {

       stage('SonarQube Analysis') {
    steps {
        withSonarQubeEnv('SonarQube') {
            bat 'cmd /c ""C:\\ProgramData\\sonar-scanner\\bin\\sonar-scanner.bat" -Dsonar.projectKey=proyecto2 -Dsonar.sources=. -Dsonar.host.url=http://localhost:9000"'
        }
    }
}



        stage('Build Docker Image') {
            steps {
                bat 'docker-compose build'
            }
        }

        stage('Tag Docker Image') {
            steps {
                bat 'docker tag proyecto2-ci-1-full:latest dylan226/proyecto2:ci'
            }
        }

        stage('Push Docker Image') {
            steps {
                bat 'docker push dylan226/proyecto2:ci'
            }
        }
    }
}
