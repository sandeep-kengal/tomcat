pipeline {
  agent any
	 parameters {
  choice choices: ['slave1', 'slave2'], description: 'which slave you want to run the job', name: 'Deploy'
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
		 agent { label 'built-in' }
	     steps {
		sh ''' free-h '''
           }
}
}
}
	
