pipeline {
  agent any
 // environment {
    //SONARQUBE_CREDENTIAL = credentials('Sonarqube_credential')
  //}
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
                sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=Sonar -Dsonar.projectName=Sonar -Dsonar.host.url=http://3.149.213.150:9000 -Dsonar.token=sqp_cd1bdfa275978e7e4510aac0cf2aeb41b17b539d'
        }
  }
}
