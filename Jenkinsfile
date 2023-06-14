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
        sh 'npm install'
      }
    }

    stage('Test') {
      steps {
        sh 'npm build'
      }
    }

    stage('Integration test') {
      steps {
        sh 'cp target/*.war /opt/tomcat/latest/webapps/'
      }
    }

  }
}