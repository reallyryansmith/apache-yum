pipeline {
  agent any
  stages {
    stage('begin message') {
      steps {
        echo 'Beginning of Pipeline'
      }
    }
    stage('log tail') {
      parallel {
        stage('log tail') {
          steps {
            sh 'tail /var/log/secure'
          }
        }
        stage('log tail test') {
          steps {
            fileExists 'Jenkinsfile'
          }
        }
      }
    }
  }
}