pipeline {
	//agent any
	agent {docker {image 'maven:3.6.3'}}
	stages {
		stage('Permissions') {
            steps {
                sh 'chmod 775 *'
            }
		stage('Build'){
			steps{
				sh "mvn --version"
				echo "Test"
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
