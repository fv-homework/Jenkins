pipeline {

    agent any

    stages {

        stage("Step1") {
            steps {
                cleanWs()
            }
        }

        stage("Step2") {
            environment {
                def br = sh(script:"echo '$branch' | cut -d'/' -f 2", returnStdout: true)
            } 
            steps {
                echo "branch:$branch"
                echo "branch after:$br"

            }
        }

        stage("Checkout ") {
            steps {
                sh "git clone --single-branch --branch $branch https://github.com/fv-homework/Jenkins.git"
            }
        }
        
        stage("Step3") {
            steps {
                sh(script:"sudo ./Jenkins/scripts/tagManager.sh", returnStdout: true)
            }
        }
    }
}
