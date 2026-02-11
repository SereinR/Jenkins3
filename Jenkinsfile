pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }
    stage('Build Java') {
      steps {
         sh 'javac Hello.java'
         sh 'javac Welcome.java'
      }
    }
    stage('Run') {
      steps {
         sh 'java Hello'
         sh 'java Welcome'
      }
    }
  }
  post {
    success { echo 'SUCCESS ' }
    failure { echo 'FAILURE ' }
  }
}
