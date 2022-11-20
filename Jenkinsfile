pipeline {
  agent any
  stages {
    stage ('git') {
      steps {
       git credentialsId: 'java-git-private-repo', url: 'https://github.com/sandeep-kengal/java.git'
      }
    }
    stage ('build') {
      steps {
       sh '''mvn clean install'''          
      }
    }
  }
}
