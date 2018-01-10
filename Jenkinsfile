pipeline {
  agent any
  stages {
    stage('present directory check') {
      parallel {
        stage('present directory check') {
          steps {
            echo 'current directory is '
            sh 'pwd'
          }
        }
        stage('connect to terraform') {
          steps {
            sh '''cd /var/lib/jenkins/test
sudo cp /var/lib/jenkins/test/pro/variables.tf ./
ll
'''
            sleep 10
          }
        }
        stage('execute infra code') {
          steps {
            echo 'executing infra code'
            sh '''pwd
'''
          }
        }
      }
    }
  }
}