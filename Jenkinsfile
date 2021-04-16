@Library('groovy-lib')_

pipeline {

    agent any
    
    stages {
        stage("ERROR HANDLER") {
            steps {
                sh "pwd"

                script {

                    gitUtils.checkout("errorHandler")
                    
                }

      

            }
        }
    }
}