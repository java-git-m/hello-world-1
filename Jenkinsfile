pipeline {
    agent any
    
    parameters{
    choice(choices: ['dev', 'qa', 'intg', 'uat'], description: 'select env', name: 'env')
    [$class: 'CascadeChoiceParameter', choiceType: 'PT_CHECKBOX', description: 'Add Description', filterLength: 1, filterable: false, 
name: 'envList', randomName: 'choice-parameter-14913050859664', referencedParameters: 'env', 
script: [$class: 'GroovyScript', fallbackScript: [classpath: [], sandbox: false, script: ''], 
script: [classpath: [], sandbox: false, script: '''if(env.equals(\'dev\')){
return[\'a1\',\'b1\',\'c1\',\'d1\']}
if(env.equals(\'qa\')){
return[\'a2\',\'b2\',\'c2\',\'d2\']}
if(env.equals(\'uat\')){
return[\'a3\',\'b3\',\'c3\',\'d3\']}
else{
return[\'a4\',\'b4\',\'c4\',\'d4\']
}''']]]  
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
