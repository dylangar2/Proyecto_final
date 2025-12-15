pipeline {
    agent any

    environment {
        // Aquí puedes poner variables de SonarQube si las tienes configuradas en Jenkins
        SONAR_SCANNER = "C:\\ProgramData\\sonar-scanner\\bin\\sonar-scanner.bat"
        PROJECT_KEY = "proyecto2"
        PROJECT_NAME = "Proyecto 2"
        PROJECT_VERSION = "1.0"
        SONAR_HOST_URL = "http://localhost:9000" // Cambia a tu URL de SonarQube
        SONAR_LOGIN = "TU_TOKEN_DE_SONAR"       // Cambia por tu token de SonarQube
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/dylangar2/proyecto2.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Aquí iría tu compilación o build si aplica'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                // Ejecuta SonarScanner con la ruta corregida
                bat "${env.SONAR_SCANNER} -Dsonar.projectKey=${env.PROJECT_KEY} -Dsonar.projectName=${env.PROJECT_NAME} -Dsonar.projectVersion=${env.PROJECT_VERSION} -Dsonar.sources=. -Dsonar.host.url=${env.SONAR_HOST_URL} -Dsonar.login=${env.SONAR_LOGIN}"
            }
        }
    }

    post {
        success {
            echo 'Pipeline completado con éxito.'
        }
        failure {
            echo 'Pipeline falló. Revisa los logs.'
        }
    }
}
