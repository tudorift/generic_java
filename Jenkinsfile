node{
	environment {
        MAVEN_HOME = '/user/lib/mvn/apache-maven-3.5.4'
		PATH = "$MAVEN_HOME/bin:$PATH"
    }
	stage 'source code'
	git credentialsId: 'github-personal', url: 'https://github.com/tudorift/generic_java.git'
	
	stage 'build and package'
	sh 'mvn clean package'
}