pipeline {
  agent any
  stages {
    stage('First') {
      parallel {
        stage('First') {
          steps {
            echo 'Hello World!'
          }
        }
        stage('Second') {
          steps {
            echo 'Welcome to Jenkins'
          }
        }
      }
    }
    stage('Third') {
      steps {
        sh 'ls -lh'
      }
    }
  }
}