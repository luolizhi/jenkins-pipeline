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
      parallel {
        stage('Test') {
          steps {
            echo 'Testing'
          }
        }
        stage('Platform1') {
          steps {
            echo 'platform1'
          }
        }
        stage('Platform2') {
          steps {
            echo 'platform2'
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying'
        kubernetesDeploy()
      }
    }
  }
  post {
    always {
      echo 'This will always run'

    }

    success {
      echo 'This will run only if successful'

    }

    failure {
      echo 'This will run only if failed'

    }

    unstable {
      echo 'This will run only if the run was marked as unstable'

    }

    changed {
      echo 'This will run only if the state of the Pipeline has changed'
      echo 'For example, if the Pipeline was previously failing but is now successful'

    }

  }
}