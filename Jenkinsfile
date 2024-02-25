pipeline {
	agent any 
	triggers {
  pollSCM '* * * * *'
}
	parameters {
	  choice choices: ['DEV', 'QA ', 'UAT', 'PROD'], name: 'Environment'
}
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
		 stage('slack-notification'){
		   steps {
                   slackSend baseUrl: 'https://hooks.slack.com/services/', channel: '#devops', color: 'good', message: 'This is for Slack', teamDomain: 'student', tokenCredentialId: 'Slack'
                   }}
}}
