pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code from Git'
                checkout scm
            }
        }

        stage('Compile') {
            steps {
                echo 'Compiling Java code'
                sh 'javac Hello.java'
            }
        }

        stage('Archive Artifacts') {
            steps {
                echo 'Archiving build outputs'
                archiveArtifacts artifacts: '*.class', fingerprint: true
            }
        }
    }

    post {
        success {
            echo 'CI PIPELINE SUCCESSFUL ✅'
        }
        failure {
            echo 'CI PIPELINE FAILED ❌'
        }
    }
}
