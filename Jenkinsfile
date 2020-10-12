pipeline {
    agent any
    tools {
        maven 'Maven 3.6.3'
    }
    stages {
        stage("maven package") {
            steps {
                dir(example) {
                    echo 'Building the application..'
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
