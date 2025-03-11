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
                sh mvn clean verify sonar:sonar -Dsonar.projectKey=Sonar-Jenkins_1 -Dsonar.projectName=Sonar-Jenkins1 -Dsonar.host.url=http://3.149.213.150:9000 -Dsonar.token=sqp_b51a673710aa7d2f3dd8a5327a617c58cf6197a8
        }
  }
}
