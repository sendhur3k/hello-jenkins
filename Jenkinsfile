pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building application'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests'
                // Uncomment next line to simulate failure
                // error "Test failed"
            }
        }
    }

    post {
        success {
            echo 'BUILD SUCCESSFUL ✅'
        }
        failure {
            echo 'BUILD FAILED ❌'
        }
        always {
            echo 'Build completed (success or failure)'
        }
    }
}
