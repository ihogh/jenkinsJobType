pipeline {
    agent { docker { image 'maven:3.8.7-eclipse-temurin-11' } }
    tools {
        maven 'maven'
    }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
                sh 'mvn clean'
                sh 'mvn compile'
                sh 'mvn test'
                sh 'mvn package'
            }            
        }
        stage('sys check') {
            steps {
                sh 'lscpu'
            }
        }
    }    
    }
