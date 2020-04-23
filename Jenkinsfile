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

        stage("Build") {
            environment {
                def res = sh(script:"bash ./Jenkins/scripts/tagManager.sh", returnStdout: true).trim()
            }
            steps {
                echo "$res"
            }
        }

        stage("Build 2") {
            steps {
                script {
                    try {
                        sh '''
                            if [ ! -z "$branch" ]
                            then
                                echo "branch not empty: $branch"
                            else
                                echo "branch is empty"
                            fi
                        '''
                    } catch (Exception e) {
                        sh "BUILD 2 is failed"
                    }
                }
            }
        }
    }
}
