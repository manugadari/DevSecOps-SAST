pipeline {
  agent any

  stages {
    stage('SAST and SCA SCANNING') {
      steps {
             sh 'snyk code test>>sastreport.txt'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying...'
      }
    }
  }
}
