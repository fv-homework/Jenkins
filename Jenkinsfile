pipeline {

    agent any

    environment {

        def var1 = true
        def var2 = false
    }

    stages {

        stage("Step1") {
            steps {
                cleanWs()
            }
        }

        stage("Input") {
            steps {

                scripts {

                    userInput = input(
                 id: 'userInput', message: 'Enter path of test reports:?', 
                 parameters: [
                 [$class: 'TextParameterDefinition', defaultValue: 'None', 
                    description: 'Path of config file', name: 'Config'],
                 [$class: 'TextParameterDefinition', defaultValue: 'None', 
                    description: 'Test Info file', name: 'Test']
                ])
                    echo ("IQA Sheet Path: "+userInput['Config'])
                    echo ("Test Info file path: "+userInput['Test'])
                }
            } 
        }   
    }
}
