pipeline{
	agent {
        node {
            label 'ROBOSHOP'
        }
    }
	stages {
		stage('Build') {
			steps {
                script{
                    sh """
                        echo "Building"
                    """
                }
			}
		}
		stage('Unit Test'){
			steps{
                script{
                    sh """
                        echo "Testing"
                        exit 1
                    """
                }
			}
		}
		stage('Deploy') {
			steps{
                script{
                    sh """
                        echo "Decploying"
                    """
                }
			}
		}
	}

    post {
        always {
            echo "I will run always"
        }

        success {
            echo "I will run only if success"
        }

        failure {
            echo "I will run only if failure"
        }
    }
}