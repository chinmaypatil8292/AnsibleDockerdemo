pipeline{
  agent any
  stages{
    stage('SCM Checkout'){
      steps{
        git 'https://github.com/chinmaypatil8292/AnsibleDockerdemo'
      }
    }
    stage('Execute ansible'){
      steps{
        ansiblePlaybook credentialsId: 'private-key', disableHostKeyChecking: true, installation: 'myansible', inventory: 'dev.inv', playbook: 'apacheplaybook.yml'
      }
    }
  }
}
