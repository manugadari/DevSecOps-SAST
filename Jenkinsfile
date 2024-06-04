pipeline {
  agent any

  stages {
    stage('Snyk Test using Snyk CLI') {
            steps {
                sh './snyk test'
            }
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying...'
      }
    }
}
