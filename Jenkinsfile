pipeline {
  agent any
  environment {
    DOCKER_HOST = "/home/jakub-marzewski/.docker/desktop/docker-cli.sock"
  }
  stages {
    stage("verify tooling") {
      steps {
        sh '''
          docker version
          docker info
          docker compose version 
          curl --version
          jq --version
        '''
      }
    }
  }
}