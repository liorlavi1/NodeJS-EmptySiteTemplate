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
        sh 'node server.js &'
      }
    }

    stage('Integration test') {
      steps {
        sh 'curl localhost:8080'
      }
    }

  }
}