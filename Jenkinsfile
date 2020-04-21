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

                sh "echo Cloning thread"
                sh "mkdir -p thread"
                sh "pwd"
                sh "cd thread"
                sh "git clone https://github.com/fv-homework/Threading.git ./thread"
            }
        }

        stage("Step3") {
            steps {

                sh "echo Cloning jack"
                sh "mkdir -p jack"
                sh "br=$(echo $branch | cut -d'/' -f 2)"
                sh "git clone -b $br https://github.com/fv-homework/Jenkins.git  ./jack"

            }
        }

        stage("Step4") {
            steps {

                sh "echo tag:$tag"
            }

        }
    }
}