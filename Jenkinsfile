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
  -Dsonar.projectKey=PetClinic \\
  -Dsonar.host.url=http://172.31.18.240:9000 \\
  -Dsonar.login=sqp_a097e7ee106bf8741ba50cab7c00f4a02b6286b7'''
      }
    }

  }
}