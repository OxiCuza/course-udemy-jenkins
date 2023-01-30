pipeline {
    agent any

    stages {
        stage("Say Hello") {
            steps {
                echo("Hello Jenkins Using Pipeline")
            }
        }
    }

    post {
        always {
            echo("I will always say hello again!")
        }

        success {
            echp("Yay, success")
        }

        failue {
            echo("Oh no, it is failure")
        }

        cleanup {
            echo("Don't care if success or not")
        }
    }
}