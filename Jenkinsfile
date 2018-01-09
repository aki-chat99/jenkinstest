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
            sh '''sudo cp ankit_565881_ohio.pem /home/ec2-user/demo
cd /home/ec2-user/demo
sudo ssh -i ankit_565881_ohio.pem ec2-user@172.16.0.42
'''
            sleep 10
          }
        }
        stage('execute infra code') {
          steps {
            echo 'executing infra code'
            sh '''sudo terraform init
sudo terraform apply
sudo rm ankit_565881_ohio.pem
exit
exit
'''
          }
        }
      }
    }
  }
}