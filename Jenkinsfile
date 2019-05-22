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
        sh '''cd /var/lib/jenkins/workspace/karate-gatling-demo_master/target/gatling/
tree '''
      }
    }
  }
}