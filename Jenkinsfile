pipeline {
	agent any
	stages {
		stage('Build') {
		steps {
			sh 'mvn clean package'
		}
		post {
			success{
				echo 'Now Archiving Files...'
				archiveArtifacts artifacts : '**/target/*.war'
			}
		}
	}	
     }
}	
