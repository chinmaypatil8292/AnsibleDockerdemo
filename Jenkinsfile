pipeline{
  agent any
  stages{
    stage('SCM Checkout'){
      steps{
        git clone 'https://github.com/chinmaypatil8292/AnsibleDockerdemo.git'
      }
    }
    stage('Execute ansible'){
      steps{
        ansiblePlaybook credentialsId: 'private-key', disableHostKeyChecking: true, installation: 'myansible', inventory: 'dev.inv', playbook: 'apacheplaybook.yml'
      }
    }
  }
}
