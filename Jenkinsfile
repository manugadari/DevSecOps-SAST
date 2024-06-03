pipeline {
  agent any
  tools { 
        maven 'MAVEN'  
    }
   stages{
    stage('Run SCA Analysis using Snyk') {
            steps {		
			withCredentials([string(credentialsId: 'SNYK_TOKEN', variable: 'SNYK_TOKEN')]) {
			    sh 'mvn snyk:test'
				}
			}
	    stage('Test') {
      steps {
        echo 'Testing...'
        snykSecurity(
          snykInstallation: 'SNYK',
          snykTokenId: 'SNYK_TOKEN',
        )
      }
    }
    }	


  }
}
