pipeline{
    agent any
    stages{
        stage('front-end'){
            agent {
                docker{image 'node:16-alpine'}
            }
        steps{ sh 'npm install'}
        }
        stage('back-end'){
            agent {
                docker{image 'maven:3.8.1-adoptopenjdk-11'}
            }
        steps{ sh 'mvn clean install'}
        }
    }
}