pipeline {
    agent any
    tools {
        jdk 'JDK_17'           
        maven 'Maven-3.9.9'    
    }
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/JamieJay1/docker-spring-boot-java-web-service.git', branch: 'main'
            }
        }
        stage('Build') {
            steps {
                bat 'echo %JAVA_HOME%'
                bat 'if not defined JAVA_HOME exit /b 1'  // Ensures JAVA_HOME is set
                bat 'mvn clean install'
            }
        }
    }
}
