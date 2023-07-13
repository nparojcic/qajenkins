pipeline {
  agent any
  stages {
    stage("Build scripts"){
      steps {
        sh "mkdir jenkinsbuild || true"
        sh "touch script1.sh"
        sh "echo 'echo this is script 1 running!' > script1.sh"
        sh "touch script2.sh"
        sh "echo 'echo this is script 2 running!' > script2.sh"
        sh "chmod+x script1.sh | chmod+x script2.sh"
      }
    }
    stage ("Test") {
      steps {
        sh "echo testing the build!"
        sh "./script1.sh"
      }
    }
    stage ("Deploy") {
      steps {
        sh "./script2.sh"
      }
    }
  }
}
