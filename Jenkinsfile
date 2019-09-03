pipeline {
    agent any
    stages {
        stage('git-checkout') {
            steps {
                git 'https://github.com/katastreet/jenkins_test'
            }
        }

        stage('Docker-build') {
            steps {
                sh label: '', script: 'docker ps'
		sh label: '', script: 'ls'
            }
        }

        stage('Docker run') {
            steps {
                sh label: '', script: 'docker ps'
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
