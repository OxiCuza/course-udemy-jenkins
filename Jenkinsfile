pipeline {
    agent any

    stages {
        stage("Build") {
            steps {
                echo("Hello Jenkins this is Build stages")
            }
        }
        stage("Test") {
            steps {
                echo("Hello Jenkins this is Test stages")
            }
        }
        stage("Deploy") {
            steps {
                echo("Hello Jenkins this is Deploy stages")
            }
        }
    }

    post {
        always {
            echo("I will always say hello again!")
        }

        success {
            echo("Yay, success")
        }

        failure {
            echo("Oh no, it is failure")
        }

        cleanup {
            echo("Don't care if success or not")
        }
    }
}