pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'hostname'
        sh 'pwd'
        sh 'whoami'
        sh 'ifconfig'
        sh 'printenv'
      }
    }
    stage('Test') {
      steps {
        echo 'Testing'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying'
      }
    }
  }
}