node{
	stage 'source code'
	git credentialsId: 'github-personal', url: 'https://github.com/tudorift/generic_java.git'
	
	stage 'build and package'
	sh 'mvn clean package'
}