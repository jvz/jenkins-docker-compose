pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'docker run --rm -v $PWD:/src docker/compose:1.24.1 -f /src/docker-compose.yml build'
      }
    }

  }
}