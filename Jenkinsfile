pipeline {
  agent any
  stages {
    stage('DEV') {
      parallel {
        stage('sonarqube') {
          steps {
            registerWebhook()
          }
        }
        stage('paso 2') {
          steps {
            sh 'ls'
          }
        }
      }
    }
  }
}