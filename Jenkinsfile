pipeline {
  agent any
    stages {
        stage('build') {
             steps{
                script{
                    sh "ansible-playbook Ansible/build.yml -i Ansible/inventory/host.yml "
                }
            }
        }
       }
      }
