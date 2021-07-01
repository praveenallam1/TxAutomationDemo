pipeline {
  agent any
  stages {
    stage('Automation- Jobs') {
      parallel {
        stage('Build-Jobs') {
          steps {
            build '1 RunDevelopmentProjectBuild'
          }
        }

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