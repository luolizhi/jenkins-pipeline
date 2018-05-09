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
  post {
		always {
			echo 'This will always run'
			//mail to: 'lzluo@chutianyun.gov.cn',
            //subject: "Failed Pipeline: ${currentBuild.fullDisplayName}",
            //body: "Something is wrong with ${env.BUILD_URL}"
		}
		success {
			echo 'This will run only if successful'
		}
		failure {
			echo 'This will run only if failed'
			//mail to: lzluo@chutianyun.gov.cn, subject: 'failed'
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
