pipeline {
  agent any
  stages {
    stage('Git clone and version manage') {
      steps {
        sh 'mvn clean test-compile gatling:test'
      }
    }
    stage('Build image') {
      steps {
        sh '''cd /var/lib/jenkins/workspace/karate-gatling-demo_master/target/
tree '''
      }
    }
    stage('Deploy to RKE') {
      steps {
        sh 'mvn clean test-compile gatling:test'
      }
    }
    stage('Function test') {
      steps {
        sh 'mvn clean test-compile gatling:test'
      }
    }
    stage('Performance test') {
      steps {
        sh 'mvn clean test-compile gatling:test'
      }
    }
    stage('Report') {
      steps {
        sh '''cd /var/lib/jenkins/workspace/karate-gatling-demo_master/target/
tree '''
      }
    }
  }
}