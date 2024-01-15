pipeline {
    agent any
  
    stages {
        stage('Clonar repositório') {
          steps {
            git branch: 'main', url: 'https://github.com/CarlosHenrryque/testes-e2e-ebac-shop.git'
            }
        }

        stage('Instalar dependencias') {
          steps {
              sh 'npm install'
            }
        }

        stage('Subir servidor') {
          steps {
            sh 'npm start'
            }
        }

        stage('Realizar os testes') {
          steps {
            sh 'NO_COLOR npm run cy:run-ci'
            }
        }
    }
}