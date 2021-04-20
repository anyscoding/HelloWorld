pipeline {
	agent {
		any 'python:3.9.4'
	}
	environment {
		DISABLE_AUTH = 'true'
		DB_ENGINE    = 'sqlite'
	}
	stages {
		stage('hello') {
			steps {
				sh 'printenv'
			}
		}
		stage('build') {
			steps {
				sh 'echo "this is stage build version: $version"'
			}
		}
		stage('test') {
			steps {
				sh 'echo "this is stage test, test switch $runUT"'
			}
		}
		stage('deploy') {
			steps {
				echo 'and this is last stage deployment'
			}
		}
	}
}
