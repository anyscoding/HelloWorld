pipeline {
	agent {
		any 'python:3.5.1'
	}
	stages {
		stage('hello') {
			steps {
				echo 'Hello World!'
			}
		}
		stage('build') {
			steps {
				echo 'this is stage build'
			}
		}
		stage('test') {
			steps {
				echo 'this is stage test'
			}
		}
		stage('deploy') {
			steps {
				echo 'and this is last stage deployment'
			}
		}
	}
}
