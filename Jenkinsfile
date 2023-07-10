pipeline {
    agent any
    stages {
        stage('Clone repo') {
            steps {
                git url:'https://github.com/malekalghraba/myapp', branch: 'main'
            }
        }

        stage('Build frontend') {
            steps {
                
                    sh '/usr/bin/npm install'
                    sh '/usr/bin/npm run build'
                
            }
        }
    

        stage('build'){  

steps{ 

sh 'ansible-playbook ansible/build.yml -i ansible/inventory/host.yml'

}   } 


   
     stage('docker'){
             steps{ 


       sh "ansible-playbook ansible/docker.yml -i ansible/inventory/host.yml "


}
       }
       
}
}
