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
				sh 'echo "this is stage build DB_ENGINE: $DISABLE_AUTH, DB_ENGINE: $DB_ENGINE"'
				sh 'ls'
				sh 'cat README.md'
				sh 'cat newfile'
			}
		}
		stage('test') {
			steps {
				sh 'echo "this is stage test"'
			}
		}
		stage('deploy') {
			steps {
				echo 'and this is last stage deployment'
			}
		}
	}
}
