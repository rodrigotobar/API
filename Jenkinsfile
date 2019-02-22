pipeline {
  agent any
  stages {
    stage('DEV') {
      parallel {
        stage('sonarqube') {
          steps {
            script { 
              hook = registerWebhook()
              echo "Waiting for POST to ${hook.getURL()}"
              data = waitForWebhook hook
              echo "Webhook called with data: ${data}"
            }
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
