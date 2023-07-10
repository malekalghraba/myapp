pipeline {
    agent any
    stages {
        stage('Clone repo') {
            steps {
                git url: 'https://github.com/malekalghraba/angular', branch: 'main'
            }
        }

        stage('Build frontend') {
            steps {
                dir('FRONTEND') {
                    sh '/usr/bin/npm install'
                    sh '/usr/bin/npm run build'
                }
            }
        }
    
/*        stage('Test frontend') {
            steps {
                dir('FRONTEND') {
                    sh 'npm run test'
                }
            }
        } */
        stage('build'){  

steps{ script{

sh 'ansible-playbook ansible/build.yml -i ansible/inventry/host.yml'

}   } 


      }
     stage('docker'){ steps{ script{ 


       sh "ansible-playbook ansible/docker.yml -i ansible/inventory/host.yml '}}}
}
}
