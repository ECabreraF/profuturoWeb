pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('ChekOut') {
      steps {
        git(url: 'https://github.com/EC501368/profuturoWeb.git', branch: 'master', changelog: true)
      }
    }

    stage('Build') {
      steps {
        withEnv(["MAVEN_HOME=", "PATH+MAVEN_HOME=:${MAVEN_HOME}"]) {
           sh 'mvn test'
        }
      }
    }

  }
}
