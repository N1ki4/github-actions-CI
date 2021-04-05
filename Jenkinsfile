    pipeline {

    agent any

    stages {
      stage(‘Build’) {
        steps {
          sh '/usr/local/bin/docker-compose up --build'
        }
      }
      stage(‘Test’) {
        steps {
          sh '/usr/local/bin/docker-compose exec api python -m pytest '/src/tests/''
        }
    }
}
