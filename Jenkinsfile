pipeline {

    agent any

    stages {

        stage("Step1") {
            steps {
                cleanWs()
            }
        }

        stage("Step2") {
            steps {
                echo "branch:$branch"
                br = sh (
                    "echo '$branch' | cut -d'/' -f 2"
                )
                echo "branch after:$br"
            }
        }
    }
}
