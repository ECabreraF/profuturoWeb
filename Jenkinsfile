pipeline {
  agent any
  stages {
    stage('ChekOut') {
      steps {
        git(url: 'https://github.com/EC501368/profuturoWeb.git', branch: 'master', changelog: true)
      }
    }

    stage('Build') {
      steps {
        pwd()
        tool 'maven_maven-3.6.2'
        sh 'mvn test'
      }
    }

  }
}