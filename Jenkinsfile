pipeline {
    agent any
    stages {
      
        stage ('Build') {
            steps {
                sh 'mvn spring-boot:build-image -Dspring-boot.build-image.imageName=aymenlouhaichi/hpa:${BUILD_ID}'
                }
            }
        stage ('tag & push') {
            steps {
                sh 'docker login --username=aymenlouhaichi --password=Cheese@77232275'  
                sh 'docker tag paketobuildpacks/run:base-cnb aymenlouhaichi/hpa'
                sh 'docker push aymenlouhaichi/hpa'
            }     
            }
        }
    
    }
