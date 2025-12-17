pipeline {
  agent none
  stages {
    stage('Back-end') {
      agent {
        docker { image 'maven:3.8.6-jdk-8' }
      }
      steps {
        sh 'mvn --version'
      }
    }
    stage('Front-end') {
      agent {
        docker { image 'node:18-alpine' }
      }
      steps {
         sh 'node --version'        
      }
    }
    stage('DB') {
      agent {
        docker { image 'mysql:latest' }
      }
      steps {
        sh 'mysql --version'
      }
    }
  }
}
