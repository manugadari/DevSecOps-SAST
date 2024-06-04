pipeline {
  agent any
 
   stages{
    stage('Run SCA Analysis using Snyk') {
            steps {	
                      snykSecurity failOnError: false, failOnIssues: false, organisation: 'manugadari', snykInstallation: 'SNYK', snykTokenId: 'SNYK_API_TOKEN'
		
				}
			}


  }

