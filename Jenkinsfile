pipeline {
  agent any
    stages {
        stage('Pull') {
             steps{
                script{
                    checkout([$class: 'GitSCM', branches: [[name: '*/master']],
                        userRemoteConfigs: [[
                            url: 'https://github.com/zeinebbellahirich/Myapp.git']]])
                }
            }
        }
        stage('Install') {
	      steps {
		  script{
		      sh "npm install" 
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
			 stage('Docker') {
	      steps {
		  script{
		      sh "ansible-playbook Ansible/docker.yml -i Ansible/inventory/host.yml" 
					}
				}
			} 
      }
      }
