//DECLARATIVE

pipeline {
	agent any
	
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
		stage('Build'){
			steps{
				sh 'mvn --version'
				sh 'docker --version'
				echo "Build"
				echo "PATH : $PATH"
				echo "BUILD ID - $env.BUILD_ID"
				echo "BUILD ID - $env.BUILD_NUMBER"
				echo "BUILD TAG - $env.BUILD_TAG"
				echo "JOB NAME -  $env.JOB_NAME"
				
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