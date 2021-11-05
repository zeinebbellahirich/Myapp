pipeline {
  agent any
    stages {
        stage('build') {
             steps{
                script{
                    sh "ansible-playbook ansible/build.yml -i ansible/inventory/host.yml "
                }
            }
        }
       }
      }
