pipeline {
    agent {
        node {
            label "linux && java11"
        }
    }

    stages {
        stage("Say Hello") {
            steps {
                echo("Hello Jenkins Using Pipeline")
            }
        }
    }
}