pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        echo 'Clean'
        sh './mvnw clean compile'
      }
    }

    stage('Static Analysis') {
      steps {
        sh '''mvn clean verify sonar:sonar \\
  -Dsonar.projectKey=PetclinicApp \\
  -Dsonar.host.url=http://172.31.18.240:9000 \\
  -Dsonar.login=sqp_e0b2b9805b27043e69fb2d72b908200764a66269'''
      }
    }

  }
}