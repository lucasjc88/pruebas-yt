pipeline {
    agent any
    tools {
        maven 'Maven 3.6.3'
    }
    dir('example') {
        stages {
        
            stage("maven package") {
                steps {
                    echo 'Building the application..'
                    sh 'mvn clean package'
                    }
                }
            stage("archive") {
                steps {
                    echo 'archive the application..'
                    archive 'target/*.jar'
                }
            }
        }
    }
}
