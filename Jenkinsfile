//DECLARATIVE

pipeline {
	// agent { docker { image 'node:13.8'} }
	stages {
		stage('Build'){
			steps{
				//sh 'node --version'
				echo "Build"
				echo "PATH : $PATH"
				echo "BUILD ID : $env.BUILD_ID"
				echo "JOB NAME : $env.JOB_NAME"
				}
			}
		stage('Test'){
			steps{
				echo "Test"
				}
			}
		stage('Integration Test'){
			steps{
				echo "Integration Test"
				}
			}
		} 
		post {
			always {
				echo 'I am Awesome. I run always!'
			}
			success {
				echo 'I run when you are successful'
			}
			failure {
				echo 'I run when you fail'
			}
		}
	}