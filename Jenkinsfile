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

        stage("Interactive_Input") {
            steps {
                script {
                def userInput = input(
                 id: 'userInput', message: 'Enter path of test reports:?', 
                 parameters: [
                 [$class: 'TextParameterDefinition', defaultValue: 'None', description: 'FRAMEWORK', name: 'toolsVersion'],
                 [$class: 'TextParameterDefinition', defaultValue: 'None', description: 'ADS EXTERNAL PACKAGE', name: 'adsVersion']
                ])
                echo ("FRAMEWORK:"+userInput['toolsVersion'])
                echo ("ADS:"+userInput['adsVersion'])

                }
            }
        } 
    }
}
