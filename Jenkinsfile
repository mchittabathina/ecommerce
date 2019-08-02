pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/Ajayvarma8142/ecommerce.git', branch: 'master')
      }
    }
    stage('build') {
      steps {
        bat 'mvn test'
      }
    }
    stage('sonar') {
      steps {
        bat 'mvn sonar:sonar'
      }
    }
            stage('Ok') {
            steps {
                echo "Ok"
            }
        }
    }
   post {
    always {
        emailext body: 'A Test EMail', recipientProviders: [[$class: 'DevelopersRecipientProvider'], [$class: 'RequesterRecipientProvider']], subject: 'Test'
    }

  }
}
