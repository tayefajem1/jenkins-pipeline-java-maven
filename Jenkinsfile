pipeline {
  agent any
  environment {
    SONARQUBE_CREDENTIAL = credentials('Sonarqube_credential')
  }
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
     stage ('Sonaqube for anaysis') {
            steps {
                echo 'Sonaqube for anaysis'
                sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=Sonar-Jenkins1 -Dsonar.projectName=Sonar-Jenkins -Dsonar.host.url=http://http://http://18.224.67.251:8080 -Dsonar.token=${SONARQUBE_CREDENTIAL}'
            }
        }
  }
}
