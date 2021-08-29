pipeline {
	agent any
	//agent {docker {image 'maven:3.6.3'}}
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH ="$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
		stage('Checkout'){
			steps{
				 sh "mvn --version"
				 sh "docker version"
				 echo "Build"
				 echo "$PATH"
				 echo "BUILD NUMBER -$env.BUILD_NUMBER"
				 echo "$env.JOB_NAME"

			}
		}
		stage('Compile'){
			steps{
				sh "mvn clean compile"
			}
		}
		stage('Test'){
			steps{
				sh "mvn test"
			}
		}
		stage('Integration Test'){
			steps{
				sh "mvn failsafe:integration-test failsafe:verify"
			}
		}
	}
}
// pipeline {
// 	agent any
// 	stages {
// 		stage('Build') {
// 			steps {
// 				echo "Build"
// 			}
// 		}
// 		stage('Test') {
// 			steps {
// 				echo "Test"
// 			}
// 		}
// 	}
// }
