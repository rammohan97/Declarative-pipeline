pipeline {
    agent any
    triggers {
        cron('0 3 * * 1-5')
    }

    stages {
        stage ('SCM') {
            steps {
                git branch: 'main', url: 'https://github.com/rammohan97/Declarative-pipeline.git'
            }
        }
        stage ('Build') {
            steps {
                echo "Build Step"
            }
        }
        stage ('package'){
            when {
                expression {
                    return params.branch == "release"
                }
            }
            echo 'packaging the code'

        }
    }
}
