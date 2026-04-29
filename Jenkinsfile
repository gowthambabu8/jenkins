pipeline{
	agent {
        node {
            label 'ROBOSHOP'
        }
    }

    environment {
        COURSE = "Jenkins"
    }

    options {
        disableConcurrentBuilds()
        timeout(time: 5, unit: 'MINUTES')
    }

    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }

	stages {
		stage('Build') {
			steps {
                script{
                    sh """
                        echo "Building"
                        echo "course is $COURSE"
                        sleep 10
                    """
                }
			}
		}
		stage('Unit Test'){
			steps{
                script{
                    sh """
                        echo "Testing"
                        echo "Name is ${params.PERSON}"
                        echo "Biography is ${params.BIOGRAPHY}"
                        echo "TOGGLE is ${params.TOGGLE}"
                        echo "CHOICE is ${params.CHOICE}"
                        echo "PASSWORD is ${params.PASSWORD}"
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