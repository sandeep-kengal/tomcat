pipeline {
  agent any
	 parameters {
  choice choices: ['slave1', 'slave2'], description: 'which slave you want to run the job', name: 'Deploy'
}
	environment{
	TICKET_NUMBER='Ticket123'
	}

    stages {
	stage ('git') {
	   steps {
		git 'https://github.com/sandeep-kengal/tomcat.git'     
	      }
		}
 
	  stage ('Build') {
          steps {
		sh ''' mvn clean package'''
       	}
          }
	 stage ('deploy') {
	     steps {
		sh ''' free -h '''
           }
}
}
}
	
