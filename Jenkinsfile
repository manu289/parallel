pipeline {
	agent none

	stages {
		stage ('make') {
			agent { label 'slaveforc' }
			steps {
			  	git 'https://github.com/manu289/mainrepo.git'
					sh 'make'
			}
		}
		stage ('Java Project') {
			agent { label 'slaveforjava' }
			steps {
				git 'https://github.com/manu289/hello-world.git'
				sh 'mvn clean install'
			}
		}
		
	}
}
