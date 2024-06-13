pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        git 'https://github.com/manugadari/DevSecOps-SAST'
        git branch: 'feature-1', url: 'https://github.com/manugadari/DevSecOps-SAST'
        sh'git checkout feature-1'
        sh'git diff --name-only master feature-1 '
      }
    } 
    stage('Authorize Snyk CLI') {
            steps {
                withCredentials([string(credentialsId: 'SNYK_TOKEN', variable: 'SNYK_TOKEN')]) {
                    sh 'snyk auth ${SNYK_TOKEN}'
                }
             }
          }

        stage('SAST SCAN for modified files') {
            steps {
                sh 'snyk code test '
                }
            }
    
        stage('SCA SCAN') {
            steps {
                sh 'snyk test '
                }
          }
     }
}
