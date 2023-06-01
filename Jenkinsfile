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
                
                    branch 'main' 
                   
                
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
