pipeline {
  environment {
        MAVEN_HOME = tool('M3')
    }
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
           sh '${MAVEN_HOME}/bin/mvn clean install'
      }
    }

  }
}
