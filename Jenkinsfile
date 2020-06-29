pipeline {
    agent any
    
    parameters{
    choice(choices: ['dev', 'qa', 'intg', 'uat'], description: 'select env', name: 'env')
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
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
