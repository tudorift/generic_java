pipeline{
	agent any
	
	environment {
        MAVEN_HOME = '/user/lib/mvn/apache-maven-3.5.4'
		PATH = "/user/lib/mvn/apache-maven-3.5.4/bin:$PATH"
    }
	
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
				echo "${MAVEN_HOME}"
				echo "${PATH}"
				sh 'printenv'
				sh '${MAVEN_HOME}/bin/mvn clean package'
			}
		}
	}
}