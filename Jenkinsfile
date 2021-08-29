// pipeline {
// 	//agent any
// 	agent {docker {image 'maven:3.6.3'}}
// 	stages {
// 		stage('Build'){
// 			steps{
// 				sh "mvn --version"
// 				echo "Test"
// 			}
// 		}
// 		stage('Test'){
// 			steps{
// 				echo "Build"
// 				echo "Test"
// 				echo "Integration Test"
// 			}
// 		}
// 		stage('Integration Test'){
// 			steps{
// 				echo "Build"
// 				echo "Test"
// 				echo "Integration Test"
// 			}
// 		}
// 	}
// }
pipeline {
	agent { docker {image 'maven:3.6.3'}}
	stages {
		stage('build') {
			steps {
				sh 'mvn --version'
			}
		}
	}
}
