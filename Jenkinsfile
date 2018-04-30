pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/ctpegasus/freezer', branch: 'master')
      }
    }
    stage('Check') {
      parallel {
        stage('Check') {
          steps {
            sh 'ls -lh'
          }
        }
        stage('status') {
          steps {
            sh 'git status'
          }
        }
      }
    }
    stage('Decision') {
      steps {
        waitUntil() {
          sh 'pwd'
        }

      }
    }
    stage('D2') {
      steps {
        input(message: 'Do you want really to deploy ?', id: 'delpoy01', ok: 'deployit')
      }
    }
  }
}