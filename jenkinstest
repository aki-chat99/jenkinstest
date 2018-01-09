pipeline {
  agent any
  stages {
    stage('execute terraform') {
      steps {
        echo 'executing terraform script'
        echo 'creating VPC'
        sh ''' sh /var/lib/jenkins/Jenkins/tf/jenkinstest.sh'
        sh 'pwd'
        terraform init
        terraform plan
        terraform apply
        ...
        
        
      }
    }
  }
}
