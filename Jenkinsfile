pipeline {
  agent any
  stages {
    stage('Test step') {
      steps {
        sh 'mvn clean test-compile gatling:test'
      }
    }
    stage('Report') {
      steps {
        sh '''cat /var/lib/jenkins/workspace/Mock-gatlingReport_master/target/gatling/catskaratesimulation-20190510024124746/index.html
'''
      }
    }
  }
}