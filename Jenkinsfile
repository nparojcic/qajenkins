pipeline {
  agent any
  stages {
    stage("Build scripts"){
      steps {
        sh "ls -a"
        sh "mkdir jenkinsbuild || true"
        sh "touch script1.sh | mv script1.sh jenkinsbuild"
        sh "echo 'echo this is script 1 running!' > script1.sh"
        sh "touch script2.sh | mv script2.sh jenkinsbuild"
        sh "echo 'echo this is script 2 running!' > script2.sh"
      }
    }
    stage ("Test") {
      steps {
        sh "echo testing the build!"
        sh "chmod +x script1.sh"
        sh "./script1.sh"
      }
    }
    stage ("Deploy") {
      steps {
        sh "chmod +x script2.sh"
        sh "./script2.sh"
      }
    }
  }
}
