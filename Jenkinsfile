pipeline {
    agent any
    tools {
        maven 'Maven 3.6.3'
    }
        stages {
            dir('example') {
                stage("maven package") {
                    steps {
                        echo 'Building the application..'
                        sh 'mvn clean package'
                    }
                }
            }
            dir('example') {    
                stage("archive") {
                    steps {
                        echo 'archive the application..'
                        archive 'target/*.jar'
                }
            }
        }
    }
}
