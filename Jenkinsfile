pipeline {
    agent any
    stages {
        stage('Clone repo') {
            steps {
                git url:'https://github.com/malekalghraba/myapp', branch: 'main'
            }
        }

        stage('Build fron') {
            steps {
                
                    sh '/usr/bin/npm install'
                 //   sh '/usr/bin/npm run build'
                
            }
        }
    

        stage('build'){  

steps{ 

			sh "/home/malekgh/.local/bin/ansible-playbook /home/malekgh/myapp/ansible/build.yml -i /home/malekgh/myapp/ansible/inventory/host.yml"

}   } 


  
}
}
