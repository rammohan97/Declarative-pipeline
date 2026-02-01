pipeline {
  agent any

  stages {
    stage('Static-Analysis') {
      steps {
        echo 'Static analysis'
        script {
          def inputVal = input(
            message: 'Have you performed static analysis?',
            parameters: [
              string(name: 'Value', description: 'Enter a value divisible by 3')
            ]
          )
          // If you used exactly one `string` parameter, `inputVal` is the string value.
          def num = inputVal as Integer

          if (num % 3 == 0) {
            echo "Divisible by 3"
          } else {
            // This aborts the build and prevents further stages
            error("Input value ${num} is NOT divisible by 3. Failing the build.")
          }
        }
      }
    }

    stage('Build') {
      steps {
        echo 'Build'
      }
    }

    stage('Unit Test') {
      steps {
        echo 'Unit tests'
      }
    }

    stage('Package') {
      steps {
        echo 'package'
      }
    }
  }
}
