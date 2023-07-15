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

			sh "/home/malekgh/.local/bin/ansible-playbook ansible/build.yml -i ansible/inventory/host.yml"

}   } 


  
}
}
