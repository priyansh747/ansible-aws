pipeline {
    agent any
    stages {
        stage('Ansible') {
          steps {
                  ansiblePlaybook(
                        credentialsId: 'ssh-key',
                        inventory: '${WORKSPACE}/inventory.txt',
                        playbook: '${WORKSPACE}/playbook.yml',
                        disableHostKeyChecking: true,
                        colorized: true
                  )
                }
        }
    }
}
