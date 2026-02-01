pipeline {
    agent any

    triggers {
        cron('0 3 * * 1-5')
    }

    stages {
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
            steps {
                echo 'packaging the code'
            }

        }
    }
}
