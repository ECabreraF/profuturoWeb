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
      withEnv(["MAVEN_HOME=/Users/devops/Downloads/apache-maven-3.6.2/bin","PATH+MAVEN_HOME=/Users/devops/Downloads/apache-maven-3.6.2/bin:${MAVEN_HOME}"]) {
      steps {
                   sh 'mvn test'
        }
      }
    }

  }
}
