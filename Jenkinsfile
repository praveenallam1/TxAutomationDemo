pipeline {
  agent any
  stages {
    stage('Project-Build') {
      parallel {
        stage('Project-Build') {
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

        stage('Mobile-Job') {
          steps {
            build '4 Run_Mobile_Tests'
          }
        }

        stage('Performance-Tests-Job') {
          steps {
            build '5 RunAutomationTests_Performance'
          }
        }

        stage('SonarCube-Job') {
          steps {
            build '6 RunAutomationTests_SonarQube'
          }
        }

      }
    }

  }
}