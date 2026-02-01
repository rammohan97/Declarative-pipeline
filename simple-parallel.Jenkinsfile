pipeline {
    agent any

    parameters {
        string("name: 'branch', defaultValue: 'main', description: 'Branch to fetch pipeline'")
    }


    stages {
        stage ('SCM') {
            steps {
                git branch: 'main', url: 'https://github.com/rammohan97/Declarative-pipeline.git'
            }
        }
        stage ('Parallel Phases') {
            parallel {
                stage ('Static Analysis'){
                    steps {
                        echo 'Perform static analysis'
                        sleep time: 3, unit: 'SECONDS'
                    }
                }
                stage ('Build and Test') {
                    stages {
                        stage ('Build') {
                            steps {
                                echo "Build Step"
                                 sleep time: 3, unit: 'SECONDS'
                            }
                        }
                        stage ('Unit Tests'){
                            steps {
                                echo 'Execute Unit Tests'
                                 sleep time: 3, unit: 'SECONDS'
                            }
                        }
                    }
                }
            }
    }
        stage ('package'){
            steps {
            echo 'packaging the code'
            }

        }
    }
}
