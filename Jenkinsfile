pipeline {
  agent any
 
   stages{
    stage('Run SCA Analysis using Snyk') {
            steps {		
		    snykSecurity failOnError: false, failOnIssues: false, organisation: 'devsecops', projectName: 'sast_scan', severity: 'high', snykInstallation: 'SNYK', snykTokenId: 'SNYK_API_TOKEN'
                          snyk code test
				}
			}
    }	


  }

