pipeline {
    agent any

    stages {
        stage('git') {
            steps {
               checkout scm
            }
        }
         stage('ansible-playbook') {
            steps {
                //ansiblePlaybook colorized: true, become: true, credentialsId: 'root', disableHostKeyChecking: true, installation: 'ansible', inventory: 'inventory.yml', playbook: 'cloud.yml'
                ansiblePlaybook colorized: true, installation: 'ansible', playbook: 'cloud.yml'

            }
        }
    }
}
