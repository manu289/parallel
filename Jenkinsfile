pipeline {
	agent none

	stages {
		stage ('make') {
			agent { label 'slaveforc' }
			steps {
			  	git 'https://github.com/GuruDeshmukh/Jenkinsproject2.git'
					sh 'make'
			}
		}
		stage ('Java Project') {
			agent { label 'slaveforjava' }
			steps {
				git 'https://github.com/GuruDeshmukh/Test-1.git'
				sh 'mvn clean install'
			}
		}
		
	}
}
