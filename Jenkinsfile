pipeline {
  agent any
  stages {
    stage("Build"){
      steps {
        sh "ll"
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
        sh "echo Present working directory: $(pwd)"
        sh "ll"
      }
    }
  }
}
