pipeline {
  agent any
  stages {
    stage('Project-Build') {
      parallel {
        stage('API-Job') {
          steps {
            build '2 RunAutomationTests_API'
            bat 'd: cd  d:\\TXAutomate\\ mvn test -Dcucumber.options="--tags @APItests"'
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