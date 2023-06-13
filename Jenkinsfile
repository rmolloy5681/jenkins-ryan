pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sayName "Mark"
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                requestApproval(environment: 'DEV', time: 1, unit: 'DAYS')
                echo 'Testing..'
            }
        }
        
        stage('JS Test') {
            agent {
                docker {image 'node:18' }
            }
            steps {
                dir('javascript'){
                    script{
                        sh 'npm start'
                    }
                }
             }
         }    
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
