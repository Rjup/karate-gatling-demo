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
        sh '''cd
sudo mkdir /home/centos/6mReport
sudo chmod -R ugo+rwx /home/centos/6mReport
sudo cp -R /var/lib/jenkins/workspace/Mock-gatlingReport_master/target/gatling/ /home/centos/6mReport'''
      }
    }
  }
}