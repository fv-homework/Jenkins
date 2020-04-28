pipeline {

    agent any

    environment {

        def var1 = true
        def var2 = false
    }

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

                        def list = [ "fede", "rico" ]

                        //List<String> list = new ArrayList<String>()
                        list.add("Virgili")

                        for ( String n : list) {
                            println n
                            sh "echo $n"
                        }

                    } catch (Exception e) {

                        sh "No correct"
                    }
                }
            }
        }

        stage("build")  {

            steps {

                script {

                    fastFail:true
                    try {

                        if ( "$var1" == false && "$var2" == true ) {

                            echo "false / true"

                        } else {

                            echo " true false "
                            sh "exit 0"
                            build.result=false
                        }

                    } catch (Exception e) {

                        echo "error"
                    }


                }

            }

        }
    }
}
