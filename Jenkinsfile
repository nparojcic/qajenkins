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
        sh "docker build -t --name jenkinsimage ."
      }
    }
    stage ("Deploy") {
      steps {
        sh "docker run -d jenkinsimage --name jenkinscontainer"
      }
    }
  }
}
