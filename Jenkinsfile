pipeline {
	agent any 
	
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/rahul/Documents/Extractfile/apache-maven-3.9.6/bin/mvn install'
	                 }}
		stage('Deployment'){
		   steps {
		sh 'cp target/CICD.war /home/rahul/Documents/Extractfile/apache-tomcat-9.0.85/webapps'
			}}	
}}
