pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'docker container run --rm -v $PWD:/src    docker/compose:1.24.1 build -f /src/docker-compose.yml'
      }
    }

  }
}