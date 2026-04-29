pipeline{
	agent {
        node {
            label 'ROBOSHOP'
        }
    }

    environment {
        COURSE = "Jenkins"
    }
	stages {
		stage('Build') {
			steps {
                script{
                    sh """
                        echo "Building"
                        echo "course is $COURSE"
                    """
                }
			}
		}
		stage('Unit Test'){
			steps{
                script{
                    sh """
                        echo "Testing"
                        exit 0
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