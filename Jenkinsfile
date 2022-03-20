pipeline {
  agent any
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
}