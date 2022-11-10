pipeline{
    agent any
    stages{
        stage('SCM checkout')
        {
          
            steps{
                git branch: 'main', url: 'https://github.com/karmasachin/myansible'
            }
        }
        stage('Ansible playbook')
        {
            steps{
                ansiblePlaybook credentialsId: 'ansiblehost', disableHostKeyChecking: true, installation: 'myansible', inventory: 'dev.inv', playbook: 'playbook1.yml’
            }
        }
    }
}
