pipeline {
  agent {
    docker {
      image 'docker/compose:latest'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'docker-compose build'
      }
    }

  }
}