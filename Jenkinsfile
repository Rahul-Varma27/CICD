pipeline {
	agent any 
	
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/rahul/Documents/Extractfile/apache-maven-3.9.6
/bin/mvn install'
	                 }}
		stage('Deployment'){
		   steps {
		sh 'cp target/flipkart.war /home/swapnil/Documents/DevOps-Software/apache-tomcat-9.0.79/webapps'
			}}	
}}
