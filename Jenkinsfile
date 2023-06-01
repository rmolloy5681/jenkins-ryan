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
             when {  
                
                    changeRequest target: 'main' 
                   
                
            }
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
