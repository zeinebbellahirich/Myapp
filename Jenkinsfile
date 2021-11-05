pipeline {
  agent any
    stages {
        stage('Pull') {
             steps{
                script{
                    checkout([$class: 'GitSCM', branches: [[name: '*/master']],
                        userRemoteConfigs: [[
                            url: 'https://github.com/Dhaker12/Continuous-Delivery.git']]])
                }
            }
        }
       
    stage('Build') {
				steps {
					script{
						sh "ansible-playbook Ansible/build.yml -i Ansible/inventory/host.yml " 
					}
				}
			} 
      }
      }
