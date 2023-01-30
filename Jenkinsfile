//SCRIPTED
// node {
// 	stage('Build') {
// 		echo "Build"
// 	}
// 	stage('Test') {
// 		echo "Test"
// 	}
// 	stage('Integration Test') {
// 		echo "Test"
// 	}
// }

// node {
// 	echo "Build"
// 	echo "Test"
// 	echo "Test"
// }

//DECLARATIVE
pipeline {
	// agent any
	// agent { docker { image 'maven:3.6.3' } }
	stages {
		stage('Build') {
			steps {
				// sh 'mvn --version'
				echo "Build"
				echo "$PATH"
				echo "Build Number - $env.BUILD_NUMBER"
				echo "Build Id - $env.BUILD_ID"
				echo "JOB Name - $env.JOB_NAME"
				echo "Build Tag - $env.BUILD_TAG"
				echo "Build URL - $env.BUILD_URL"
			}
		}
		stage('Test') {
			steps {
				echo "Test"
			}
		}
		stage('Integration Test') {
			steps {
				echo "Integration Test"
			}
		}
	} 
	post {
		always {
			echo 'I run always!'
		}
		success {
			echo 'I run when you are successfull!'
		}
		failure {
			echo 'I run when you fail!'
		}
	}
}