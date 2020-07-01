pipeline {
    agent any
    
  
    
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                echo "${params.Env}"
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
