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
        sh 'mvn compile'
      }
    }

    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }

    stage('Package') {
      steps {
        sh 'mvn clean package'
      }
    }

  }
}