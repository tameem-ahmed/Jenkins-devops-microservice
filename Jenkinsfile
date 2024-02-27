//DECLARATIVE

pipeline {
	agent { docker { image 'node:13'} }
	stages {
		stage('Build'){
			steps{
				sh 'node --version'
				echo "Build"
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