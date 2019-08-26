pipeline{
	agent any

	tools {
		maven 'apache-maven-3.5.4'
	}
	
	stages{ 
		stage('source code checkout'){
			steps{
				git credentialsId: 'github-personal', url: 'https://github.com/tudorift/generic_java.git'
			}
		}
		stage('Maven build and package'){
			steps{
				sh 'printenv'
				sh 'mvn clean package'
			}
		}
	}
}