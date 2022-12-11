pipeline {
  agent any

  options{
    buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr:'5', daysToKeepStr:'', numToKeepStr:'5')
    disableConcurrentBuilds()
  }

  stages {
    stage('Build') {
      steps {
        sh '''
          npm run build
        '''
      }
    }
    stage('Test') {
      steps {
        echo 'Testing...'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying on production...'
      }
    }
  }
}