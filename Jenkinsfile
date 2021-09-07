pipeline {
    agent any
    stages {
      
        stage ('Build') {
            steps {
                sh 'mvn spring-boot:build-image -Dspring-boot.build-image.imageName=springio/gs-spring-boot-docker'
                }
            }
        stage ('tag & push') {
            steps {
                sh 'docker tag paketobuildpacks/run:base-cnb aymenlouhaichi/hpa:${BUILD_ID}'
                sh 'docker tag paketobuildpacks/run:base-cnb aymenlouhaichi/hpa'
                sh 'docker push aymenlouhaichi/hpa'
                

                
            }
        }
    
    }
