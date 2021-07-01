pipeline {
  agent any
  stages {
    stage('Automation- Jobs') {
      parallel {
        stage('API-Job') {
          steps {
            build '2 RunAutomationTests_API'
          }
        }

        stage('Web-Job') {
          steps {
            build '3 RunAutomationTests_Web'
          }
        }

      }
    }

  }
}