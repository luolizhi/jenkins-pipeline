pipeline {
  agent { 
		//docker { image 'python:3.5.1' } 
		label 'jnlp-slave'
	}
  
  /*
	environment {
        AWS_ACCESS_KEY_ID     = credentials('jenkins-aws-secret-key-id')
        AWS_SECRET_ACCESS_KEY = credentials('jenkins-aws-secret-access-key')
    }
	
	parameters {
        string(name: 'Greeting', defaultValue: 'Hello', description: 'How should I greet the world?')
    }
	*/
  
  stages {
    stage('build') {
      steps {
        //sh 'python --version'
				sh 'hostname'
				sh 'pwd'
				sh 'whoami'
				sh 'ifconfig'
				sh 'printenv'
				//echo "${params.Greeting} World!"
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
