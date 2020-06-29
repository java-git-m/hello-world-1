pipeline {
    agent any
    
    parameters{
    choice(choices: ['dev', 'qa', 'intg', 'uat'], description: 'select env', name: 'env')
        if(env.equals(dev)){
            choice(choices: ['dev', 'qa', 'intg', 'uat'], description: 'select region', name: 'region')
        }
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

