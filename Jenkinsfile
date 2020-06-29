pipeline {
    agent any
    
    properties([parameters([choice(choices: ['dev', 'qa', 'intg', 'uat'], description: 'select env', name: 'env'), [$class: 'CascadeChoiceParameter', choiceType: 'PT_SINGLE_SELECT', description: '', filterLength: 1, filterable: false, name: 'envList', randomName: 'choice-parameter-1484370066993', referencedParameters: 'env', script: [$class: 'GroovyScript', fallbackScript: [classpath: [], sandbox: false, script: ''], script: [classpath: [], sandbox: false, script: '''if(env.equals(\'dev\')){
return \'A\'
else {
return \'B\'
}''']]]])])
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
