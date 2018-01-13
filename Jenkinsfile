pipeline {
  agent any
  stages {
    stage('error') {
      parallel {
        stage('error') {
          steps {
            error 'error'
          }
        }
        stage('s1') {
          steps {
            bat(script: 'echo coucou', returnStatus: true, returnStdout: true)
          }
        }
      }
    }
    stage('end') {
      steps {
        echo 'end'
      }
    }
  }
}