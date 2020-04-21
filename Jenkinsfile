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
            }
        }
    }
}
