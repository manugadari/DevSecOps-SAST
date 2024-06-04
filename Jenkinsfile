pipeline {
  agent any

  stages {
    stage('SAST and SCA SCANNING') {
      steps {
             snykSecurity failOnError: false, failOnIssues: false, monitorProjectOnBuild: false, severity: 'high', snykInstallation: 'SNYK', snykTokenId: 'SNYK_API_TOKEN'
              sh 'snyk code test>>report.txt
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying...'
      }
    }
  }
}
