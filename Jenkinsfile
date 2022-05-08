pipeline{
	agent any
	//agent { docker { image 'node:18.1.0'} }
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH="dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages{
		stage('Build') {
			steps {
				//sh 'node --version'
				//sh 'mvn --version'
				//sh 'docker --version'
				echo "$PATH"
				echo "Build number - $env.BUILD_NUMBER"
				echo "Build Id - $BUILD_ID"
				echo "Job name - $env.JOB_NAME"
				echo "Build tag - $BUILD_TAG"
				echo "Build url - $BUILD_URL"
				echo "Build"
			}
		}

		stage('Test') {
			steps {
				echo "Test sample"
			}
		}

		stage('Integration Test') {
			steps {
				echo "Integration Tests"
			}
		}
	} 
	post {
		always {
			echo 'I run always'
		}
		success {
			echo 'I run if the buid is successful'
		}
		failure {
			echo 'I run when you fail'
		}
	}
}
