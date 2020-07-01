


properties([parameters([[$class: 'ChoiceParameter', choiceType: 'PT_SINGLE_SELECT', description: 'Please select Environment', filterLength: 1, filterable: false, name: 'Environment', randomName: 'choice-parameter-29457514670285', script: [$class: 'GroovyScript', fallbackScript: [classpath: [], sandbox: false, script: 'return ["error"]'], script: [classpath: [], sandbox: false, script: 'return[\' \',\'dev\',\'qa\']']]], [$class: 'CascadeChoiceParameter', choiceType: 'PT_CHECKBOX', description: '', filterLength: 1, filterable: False, name: 'Branch', randomName: 'choice-parameter-29457526667858', referencedParameters: 'Environment', script: [$class: 'GroovyScript', fallbackScript: [classpath: [], sandbox: false, script: 'return ["unknown branch"]'], script: [classpath: [], sandbox: false, script: '''if (Environment.equals("dev")){
return["Devlopment"]
} else if (Environment.equals("qa")){
return["QA Branch"]
}else {
return["select env"]
}
''']]]])])
pipeline {
    agent any
    
  
    
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
