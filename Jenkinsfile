pipeline {
    agent any

    environment {
        AUTHOR = "Oxicusa Gugi Housman"
        WEB = "oxicuza@github.io"
    }

    parameters {
        string(name: "NAME", defaultValue: "Guest", description: "What is your name?")
        text(name: "DESCRIPTION", defaultValue: "Hehehe", description: "Tell me about you")
        booleanParam(name: "DEPLOY", defaultValue: false, description: "Need to deploy?")
        choice(name: "SOCIAL_MEDIA", choices: ['Instagram', 'Facebook'], description: "Which one?")
        password(name: "SECRET", defaultValue: "")
    }

    options {
        disableConcurentBuilds()
        timeout(time: 10, unit: 'MINUTES')
    }

    stages {
        stage("Prepare") {
            steps {
                echo("Author : ${AUTHOR}")
                echo("Start Job : ${env.JOB_NAME}")
                echo("Start Build : ${env.BUILD_NUMBER}")
                echo("Branch Name : ${env.BRANCH_NAME}")
            }
        }
        stage("Build") {
            steps {
                script {
                    for (int i = 0; i < 10; i++) {
                        echo("Script ${i}")
                    }
                }
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