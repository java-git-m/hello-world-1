
pipeline {
    agent any
    
  parameters {
      activeChoiceParam('States') {
        description('Name of the State')
        filterable() 
        choiceType('SINGLE_SELECT')
        groovyScript {
          script('return ["Sao Paulo", "Rio de Janeiro"]')
          fallbackScript('"Error in script"')
        }
      }
      activeChoiceReactiveParam('Cities') {
        description('Name of the State')
        filterable() 
        choiceType('SINGLE_SELECT')
        referencedParameters('States')
        groovyScript {
          script('if (States.equals("Sao Paulo") { return ["Itu", "Araras"] } else { return ["Angra dos Reis"] }')
          fallbackScript('"Error in script"')
        }
      }
  }
    
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                echo "${params.States}"
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
