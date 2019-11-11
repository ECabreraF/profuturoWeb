pipeline {
  agent any
  stages {
    stage('ChekOut') {
      steps {
        git(url: 'https://github.com/EC501368/profuturoWeb.git', branch: 'master', changelog: true)
      }
    }

  }
}