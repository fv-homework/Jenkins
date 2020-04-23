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

        stage("Step2") {
            environment {
                def br = sh(script:"echo '$branch' | cut -d'/' -f 2", returnStdout: true)
            } 
            steps {
                sh(script:"./scripts/tagManager.sh", returnStdout: true)
            }
        }
    }
}
