pipeline {
	agent any
	//agent {docker {image 'maven:3.6.3'}}
	enviroment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH ="$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
		stage('Build'){
			steps{
				 sh "mvn --version"
				 sh "docker version"
				 echo "Build"
				 echo "$PATH"
				 echo "BUILD NUMBER -$env.BUILD_NUMBER"
				 echo "$env.JOB_NAME"

			}
		}
		stage('Test'){
			steps{
				echo "Build"
				echo "Test"
				echo "Integration Test"
			}
		}
		stage('Integration Test'){
			steps{
				echo "Build"
				echo "Test"
				echo "Integration Test"
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
