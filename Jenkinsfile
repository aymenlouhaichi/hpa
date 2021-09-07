pipeline {
    agent any
    stages {
      
        stage ('Build') {
            steps {
                sh 'mvn spring-boot:build-image -Dspring-boot.build-image.imageName=springio/gs-spring-boot-docker'
                }
            }
        }
    }
