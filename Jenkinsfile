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
                def br = sh(script:"echo '$branch' | cut -d'/' -f 2", returnStdout: true)
                echo "branch after:$br"
            }
        }
    }
}
