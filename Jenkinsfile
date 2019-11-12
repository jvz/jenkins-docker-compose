pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t jenkins-compose-build .'
        sh 'docker run --rm jenkins-compose-build build'
      }
    }

  }
}
