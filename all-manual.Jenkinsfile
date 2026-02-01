pipeline {
    agent any

    stages {
        stage ('Static-Analysis'){
            steps {
                echo 'Static analysis'

                script{
                    input message : "Have u performed static analysis ?", 
                    ok: "Yes"
                }
            }
        }
        stage ('Build'){
                steps {
                    echo 'Build'
                }
            }
        stage ('Unit Test'){
                steps {
                    echo 'Unit tests'
                }
            }
        stage ('Package'){
                steps {
                    echo 'package'
            }
        }
    }
}
