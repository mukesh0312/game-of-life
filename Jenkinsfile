pipeline {
	agent { label 'jdk17' }
	stages {
		stage ('source code') {
			steps {
				git 'https://github.com/wakaleo/game-of-life.git'
			}
		}
		
		stage ('build') {
			steps {
				sh 'mvn compile'
			}
		}
		
		stage ('unittest and arcive .jar file') {
			steps {
				junit '**/surefire-reports/*.xml
			}
		}
	}

    
}
