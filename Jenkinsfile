pipeline {
    agent any
    tools {
        maven 'Maven 3.6.3'
    }
    stages {
        stage("maven package") {
            dir('example') {
                steps {
                    echo 'Building the application..'
                    sh 'mvn clean package'
                }
            }
        }   
        stage("archive") {
            dir('example') { 
                steps {
                    echo 'archive the application..'
                    archive 'target/*.jar'
                }
            }
        }
    }
}
