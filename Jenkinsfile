pipeline {
    agent any
    stages {
        stage('compile') {
            steps {
                echo "Compiled successfully";
            }
        }

        stage('JUnit') {
            steps {
                echo "Junit passed successfully";
            }
        }

        stage('Quality-Gate') {
            steps {
                echo "Quality gate passed successfully";
            }
        }

        stage('Deploy') {
            steps {
                echo "Successfully deployed";
            }
        }
    }

    post {
        always {
            echo "This will always run"
        }
        success {
            echo "This will run if successful"
        }
        failure {
            echo "This will run if failed"
        }
        unstable {
            echo "This will run if marked unstable"
        }
        changed {
            echo "This will run if state of pipeline changed i.e. previously failing but successful now or viceversa"
        }
    }
}