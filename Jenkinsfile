pipeline {
  agent any
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
			
       parameters {
  choice choices: ['slave1', 'slave2'], description: 'which slave you want to run the job', name: 'Deploy'
}



	  stage ('deploy') {

            agent ${params.Deploy}

	     steps {

				sh ''' free-h '''
           }
}
}
}
         	
