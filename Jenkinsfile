pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'docker build -f Dockerfile.build .'
      }
    }

  }
  environment {
    DOCKER_HOST = 'tcp://docker:2376'
  }
}