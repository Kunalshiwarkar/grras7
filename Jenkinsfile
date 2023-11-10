pipeline {
	agent any triggers {
  pollSCM '* * * * *'
}
       parameters {
		choice(name: 'ENVIRONMENT', choices: ['QA','UAT'], description: 'Pick Environment value')
	}
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/grras/slave-dir/apache-maven-3.9.5/bin/mvn instal'
	                 }}
		stage('Deployment'){
		   steps {
		sh 'cp target/grras7.war /home/gras/slave-dir/apache-tomcat-9.0.82/webapps'
			}}	
}}
