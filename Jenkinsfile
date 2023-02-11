pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        echo 'Clean'
        sh './mvnw clean compile'
      }
    }

  }
}