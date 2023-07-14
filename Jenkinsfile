 pipeline {
  agent any
  stages {
    stage("Cleanup"){
      steps {
        sh "docker system prune -a"
      }
    }
    stage ("Build") {
      steps {
        sh "docker build -t task1image -f Dockerfile ."
      }
    }
    stage ("Deploy") {
      steps {
        sh "docker run -d task1image --name jenkinscontainer"
      }
    }
  }
}
