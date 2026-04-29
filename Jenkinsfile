pipeline{
	agent any
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
}