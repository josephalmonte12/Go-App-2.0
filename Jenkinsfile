pipeline {
    agent any
    
    environment {
        // Define las variables de entorno necesarias para tu pipeline
    }
    
    stages {
        stage('Checkout') {
            steps {
                // Paso para clonar el repositorio
                checkout scm
            }
        }
        
        stage('Build') {
            steps {
                // Paso para construir la aplicación Go
                sh 'go build -o myapp'
            }
        }
        
        stage('Test') {
            steps {
                // Paso para ejecutar pruebas de la aplicación Go
                sh 'go test ./...'
            }
        }
        
        stage('Deploy') {
            steps {
                // Paso para desplegar la aplicación
                // Aquí podrías usar Docker, Docker Compose, Kubernetes u otras herramientas según tu entorno de despliegue
                sh 'docker-compose up -d'
            }
        }
    }
    
    post {
        success {
            // Acciones a realizar si el pipeline tiene éxito
            echo '¡El pipeline se ejecutó con éxito!'
        }
        
        failure {
            // Acciones a realizar si el pipeline falla
            echo '¡El pipeline falló! Revisar los registros para más detalles.'
        }
    }
}
