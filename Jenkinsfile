pipeline {
    agent any

    stages {
        stage('Git Clone') {
            steps {
               git credentialsId: 'Github_Login', url: 'https://github.com/ANandhish/java-tomcat-maven-example.git'
            }
        }
        stage('Build') {
            steps {
                bat 'mvn clean install sonar:sonar'
            } 
        }
    }
}
