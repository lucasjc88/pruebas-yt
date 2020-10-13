pipeline {
    agent any
    tools {
        maven 'Maven 3.6.3'
    }
    stages {
        stage("maven package") {
            steps {
                dir('example') {
                    echo 'Building the application..'
                    sh 'mvn clean package'
                }
            }
        }   
        stage("archive") {
            steps {
                dir('example') {
                    echo 'archive the application..'
                    archive 'target/*.jar'
                }
            }
        }
    }
}
