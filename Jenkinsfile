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
                sh "echo 'jekins file'"
                sh "echo $branch"

                sh "mkdir -p thread"
                sh "pwd"
                sh "cd thread"
                sh "git clone https://github.com/fv-homework/Threading.git"
            }
        }

        stage("Step3") {
            steps {
                sh "pwd"
            }
        }

        stage("Step4") {
            steps {
                sh "echo $tag"
            }

        }
    }
}