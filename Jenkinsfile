pipeline {
    agent any

    stages {
        stage("Build") {
            steps {
                echo("Start Build")
                sh("./mvnw clean compile test-compile")
                echo("Finish Build")
            }
        }
        stage("Test") {
            steps {
                echo("Start Test")
                sh("./mvnw test")
                echo("Finish Test")
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