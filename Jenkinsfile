pipeline {
  agent {
    node {
      label 'docker'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }

    stage('Test') {
      steps {
        sh 'npm run test'
      }
    }

    stage('Deliver') {
      steps {
        sh 'npm run build'
        sh 'npm run start'
      }
    }

  }
  environment {
    image = 'node:lts-buster-slim'
    args = '-p 3000:3000'
  }
}