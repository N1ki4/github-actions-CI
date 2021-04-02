pipeline {
    agent any

    stages("build app") { 
      steps {
        sh "docker-compose up -d --build"
      }
    }

    stages("run tests") {
      steps {
        sh """
          docker-compose exec api python -m pytest 'src/tests'
          """
      }
    }
}
