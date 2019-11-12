pipeline {
  agent {
    docker {
      image 'docker/compose:1.24.1'
      args 'build'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'build'
      }
    }

  }
}