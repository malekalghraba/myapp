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
                
                    sh 'npm install'
                    sh 'npm run build'
                
            }
        }
    

        stage('build'){  

steps{ 

sh 'ansible-playbook ansible/build.yml -i ansible/inventry/host.yml'

}   } 


   
     stage('docker'){
             steps{ 


       sh "ansible-playbook ansible/docker.yml -i ansible/inventory/host.yml "


}
       }
       
}
}
