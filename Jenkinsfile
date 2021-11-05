pipeline {
  agent any
    stages {
        stage('build') {
             steps{
                script{
                    sh "ansible-playbook ansible/build.yml -i Ansible/inventory/host.yml "
                }
            }
        }
       }
      }
