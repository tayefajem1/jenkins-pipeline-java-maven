pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh 'mvn clean install'
      }
    }
    stage('Unit Test') {
      steps {
        sh 'mvn clean test'
      }
    }
    stage('Sonarqube') {
      steps {
        echo "Sonarqube Scanner"
        sh 'mvn clean verify sonar:sonar  -Dsonar.projectKey=Sonar -Dsonar.projectName=Sonar -Dsonar.host.url=http://3.149.213.150:9000 -Dsonar.token=sqp_cd1bdfa275978e7e4510aac0cf2aeb41b17b539d'
      }
    }
    
  }
}
