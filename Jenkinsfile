pipeline {
  agent any
 
   stages{
    stage('Run SCA Analysis using Snyk') {
            steps {		
			withCredentials([string(credentialsId: 'SNYK_TOKEN', variable: 'SNYK_TOKEN')]) {
			    sh 'snyk test'
				}
			}
    }	


  }
}
