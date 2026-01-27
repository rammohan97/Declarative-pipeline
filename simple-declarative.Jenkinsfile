pipeline {
    agent any
    environment {
        STRING = "Need to change immediately"
    }
    stages {
        stage ('Hello') {
            steps {
                echo 'Hello Jenkins!!'
                script {
                    def words = env.STRING.split(' ')
                    for (word in words){
                        echo word
                    }
                }
            }
        }
    }
}
