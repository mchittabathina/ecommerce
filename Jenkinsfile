pipeline {
  agent any
  stages {
    stage('code pull') {
      steps {
        git 'https://github.com/krishna7362/ecommerce.git'
      }
    }
    stage('build') {
      steps {
        bat 'mvn install'
      }
    }
  }
}