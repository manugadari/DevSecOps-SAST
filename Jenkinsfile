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
        snykSecurity(
          snykInstallation: '<SNYK>',
          snykTokenId: '<SNYK_API_TOKEN>',
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
