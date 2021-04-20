pipeline {
	agent {
		docker {
			image 'maven:3.8.1-adoptopenjdk-11'
        		label 'my-defined-label'
        		args  '-v /tmp:/tmp'
		}
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
