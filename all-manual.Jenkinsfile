pipeline {
    agent any

    stages {
        stage ('Static-Analysis'){
            steps {
                echo 'Static analysis'

                script{
                    def number = input (
                        message : "Have u performed static analysis ?", 
                        parameters:[
                            string(name: 'Value', description: 'Enter a value divisible by 3')
                        ]
                    )
                    def num = number.toInteger()
                    if (num % 3 == 0){
                        echo "divisible by 3"
                    }else{
                        echo "Not divisible by 3"
                    }
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
