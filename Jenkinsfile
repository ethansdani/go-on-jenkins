pipeline {
	agent any
	stages {
		stage ('fetching-sourcecode') {
			steps {
				echo 'Getting the soure code from GitHub'
			}
		}
		stage ('compile') {
			steps {
				echo 'Compiling the source code using maven'
			}
		}
		parallel {
			stage ('unit-test') {
				steps {
					echo 'Performing unit testing'
				}
			}
			stage ('integration-test') {
				steps {
					echo 'Perorming integration testing'
				}
			}
		}
		stage ('archiving') {
			steps {
				echo 'Archiving the artifacts'
			}
		}
		stage ('copying') {
			steps {
				echo 'Copying the artifacts'
			}
		}		
		stage ('deploy') {
			steps {
				echo 'Deploying to apache tomcat server'
			}
		}
	}
}
