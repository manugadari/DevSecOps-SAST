pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        echo 'Building...'
      }
    }
    stage('Test') {
      steps {
        echo 'Testing...'
        
          snykSecurity failOnError: false, failOnIssues: false, severity: 'critical', snykInstallation: 'SNYK', snykTokenId: 'SNYK_API_TOKEN'
        
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying...'
      }
    }
  }
}
