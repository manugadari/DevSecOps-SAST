pipeline {
  agent any
  tools {
    SNYK
  }

  stages {
    stage ('Run SAST Scan') {
      steps {
            snykSecurity failOnError: false, failOnIssues: false, organisation: 'manugadari', snykInstallation: 'SNYK', snykTokenId: 'SNYK_API_TOKEN'      }
    }
  }
}
