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
        sh '''tree /var/lib/jenkins/workspace/Mock-gatlingReport_master/target/gatling/
'''
      }
    }
  }
}