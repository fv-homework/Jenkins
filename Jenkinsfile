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


        stage("sed") {

            steps {

                script {

                    sh "cat file.xml"

                }

            }

        }

        // stage("Interactive_Input") {
        //     steps {
        //         script {
        //         echo "clone"
        //         sh "git clone https://github.com/fv-homework/Jenkins.git --branch jackparams"
        //         def xmlinput = sh(script:"cat ./Jenkins/xmlfile.xml", returnStdout: true).trim()
        //         def userInput = input(
        //          id: 'userInput', message: 'Enter path of test reports:?', 
        //          parameters: [
        //          string(defaultValue: 'None', description: 'FRAMEWORK', name: 'toolsVersion'),
        //          string(defaultValue: 'None', description: 'ADS EXTERNAL PACKAGE', name: 'adsVersion'),
        //         [$class: 'TextParameterDefinition', defaultValue: "$xmlinput", description: 'Xml show', name: 'XmlContent']

        //         ])
        //         echo ("FRAMEWORK:"+userInput['toolsVersion'])
        //         echo ("ADS:"+userInput['adsVersion'])

        //         }
        //     }
        // } 
    }
}
