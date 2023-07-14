 pipeline {
  agent any
  stages {
    stage("Cleanup"){
      steps {
        sh "echo hello"
      }
    }
    stage ("Build") {
      steps {
        sh "docker build -t task1image ."
      }
    }
    stage ("Deploy") {
      steps {
        sh "docker run -d task1image --name jenkinscontainer"
      }
    }
  }
}
