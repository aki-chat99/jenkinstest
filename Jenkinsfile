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
        stage('cp required files') {
          steps {
            sh '''cd /var/lib/jenkins/test
cp -f /var/lib/jenkins/test/pro/variables.tf ./ '''
            sleep 10
          }
        }
        stage('execute infra code') {
          steps {
            echo 'executing infra code'
            sh '''terraform init
terraform apply
rm -f /var/lib/jenkins/test/variables.tf'''
          }
        }
      }
    }
  }
}