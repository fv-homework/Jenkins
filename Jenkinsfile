pipeline {

    agent any

    stages {

        stage("Step1") {

            steps {
                sh "echo Clean workspace"
                cleanWs()
            }
        }

        stage("Step2") {
            steps {

                sh "Cloning thread"
                sh "mkdir -p thread"
                sh "pwd"
                sh "cd thread"
                sh "git clone https://github.com/fv-homework/Threading.git ./thread"
            }
        }

        stage("Step3") {
            steps {

                sh "Cloning jack"
                sh "mkdir -p jack"
                sh "clone https://github.com/fv-homework/Jenkins.git $branch ./jack"

            }
        }

        stage("Step4") {
            steps {

                sh "echo tag:$tag"
            }

        }
    }
}