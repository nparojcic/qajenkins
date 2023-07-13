pipeline {
  agent any
  stages {
    stage("Build"){
      steps {
        sh "ls -a"
        sh "mkdir jenkinsbuild || true"
        sh "touch buildfile.txt | mv jenkinsbuild" 
      }
    }
    stage ("Test") {
      steps {
        sh "echo testing the build!"
        sh "echo success"
      }
    }
    stage ("Deploy") {
      steps {
        sh "pwd"
        sh "ls -a"
      }
    }
  }
}
