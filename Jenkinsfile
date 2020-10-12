pipeline {
    agent any
    stages {
        stage("maven package") {
            steps {
                dir(example) {
                    echo 'Building the application..'
                    maven() {
                        sh 'mvn clean package'
                    }
                }
            }
        }
        /*stage("archive") {
            steps {
                echo 'testing the application..'
                archive 'example/target/*.jar'
            }
        }*/
    }
}