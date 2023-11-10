pipeline {
	agent any 

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
			  sh '/home/kunal/Documents/Devops_software/tar/apache-maven-3.9.5/bin/mvn instal'
	                 }}
		stage('Deployment'){
		   steps {
		sh 'cp target/grras7.war /home/kunal/Documents/Devops_software/tar/apache-tomcat-9.0.82/webapps'
			}}	
}}
