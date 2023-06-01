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
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
