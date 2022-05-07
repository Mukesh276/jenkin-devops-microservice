pipeline{
	agent any
	stages{
		stage('Build') {
			steps {
				echo "Build"
			}
		}

		stage('Test') {
			steps {
				echo "Test"
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
