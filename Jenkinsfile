pipeline {
  agent {
    node {
      label 'docker'
    }

  }
  stages {
    stage('Git Checkout') {
      steps {
        git(url: 'https://github.com/liorlavi1/NodeJS-EmptySiteTemplate', branch: 'master')
      }
    }

    stage('Build') {
      steps {
        sh 'mvn clean package'
      }
    }

  }
}