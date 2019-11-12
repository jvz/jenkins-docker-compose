pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'docker -H tcp://docker:2376 build -f Dockerfile.build .'
      }
    }

  }
}