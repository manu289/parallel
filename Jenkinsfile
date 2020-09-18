pipeline {
	agent none
	stages ( 'c-project and java' ) {
		parallel {
		stage ('make') {
			agent { label 'slaveforc' }
			steps {
			  	git 'https://github.com/manu289/mainrepo.git'
					sh 'make'
				echo 'This is slaveforc node with STAGE 1'
						sh 'sleep 10'
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
		
	}
}
