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
                sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=Sonar-Jenkins1 -Dsonar.projectName=Sonar-Jenkins -Dsonar.host.url=http://3.133.139.118:9000 -Dsonar.token=${SONARQUBE_CREDENTIAL}'
            }
        }
  }
}
