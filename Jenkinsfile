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
        stage('execute') {
          steps {
            sh '''cd /var/lib/jenkins/test
cp -f /var/lib/jenkins/test/pro/variables.tf ./ 
terraform init
terraform apply
rm -f /var/lib/jenkins/test/variables.tf'''
            sleep 10
          }
        }
      }
    }
  }
}