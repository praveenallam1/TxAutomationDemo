pipeline {
  agent any
  stages {
    stage('Automation- Jobs') {
      parallel {
        stage('A-Build-Jobs') {
          steps {
            build '1 RunDevelopmentProjectBuild'
          }
        }

        stage('B-API-Job') {
          steps {
            build '2 RunAutomationTests_API'
          }
        }

        stage('C-Web-Job') {
          steps {
            build '3 RunAutomationTests_Web'
          }
        }

        stage('D-Mobile-Job') {
          steps {
            build '4 Run_Mobile_Tests'
          }
        }

        stage('E-Performance-Job') {
          steps {
            build '5 RunAutomationTests_Performance'
          }
        }

        stage('F-SonarCube-Job') {
          steps {
            build '6 RunAutomationTests_SonarQube'
          }
        }

      }
    }

  }
}