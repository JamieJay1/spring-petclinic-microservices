pipeline {
    agent any
    tools {
        jdk 'JDK_17'          
        maven 'Maven-3.9.9'    // Already configured
    }
    stages {
        stage('Checkout') {
            steps {
                
                git branch: 'master', url: 'https://github.com/JamieJay1/docker-spring-boot-java-web-service.git'
            }
        }
        stage('Build') {
            steps {
                
                bat 'echo %JAVA_HOME%'        // Correct Windows-style variable
                // Run Maven build
                bat 'mvn clean install'
            }
        }
    }
}
