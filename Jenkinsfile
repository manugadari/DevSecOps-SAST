pipeline {
  agent any

  stages {
    stage('SAST SCANNING') {
      steps {
        snykSecurity(
          snykInstallation: 'SNYK',
          snykTokenId: 'SNYK_API_TOKEN',
        )
          sh 'snyk code test>>sastreport.txt'
      }
    }
    stage('Test') {
      steps {
        echo 'Testing...'
        snykSecurity(
          snykInstallation: 'SNYK',
          snykTokenId: 'SNYK_API_TOKEN',
          // place other parameters here
        )
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying...'
      }
    }
  }
}
