pipeline {
  agent any

  stages {
    stage('sast scan') {
      steps {
        snykSecurity additionalArguments: 'snyk code test>>sast.txt', failOnError: false, failOnIssues: false, monitorProjectOnBuild: false, severity: 'high', snykInstallation: 'SNYK', snykTokenId: 'SNYK_API_TOKEN'
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
