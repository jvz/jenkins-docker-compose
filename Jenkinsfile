pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''env
docker -H tcp://docker:2376 build -f Dockerfile.build .'''
      }
    }

  }
}