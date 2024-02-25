pipeline {
    agent any
    
    stages {
        stage('Clonar repositorio') {
            steps {
                // Clonar el repositorio desde Git
                git 'https://github.com/josephalmonte12/Go-App-2.0'
            }
        }
        stage('Construir') {
            steps {
                // Construir la aplicación Go
                sh 'go build -o main main.go'
            }
        }
        stage('Pruebas') {
            steps {
                // Ejecutar pruebas si es necesario
                // Por ejemplo:
                // sh 'go test ./...'
            }
        }
        stage('Desplegar') {
            steps {
                // Desplegar la aplicación si es necesario
                // Por ejemplo, si estás utilizando Docker:
                // sh 'docker build -t my-go-app .'
                // sh 'docker run -d --name my-app-container my-go-app'
            }
        }
    }
}
