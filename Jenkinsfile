pipeline {
    agent any

   tools {
    jdk 'jdk-21'
    maven 'maven 3.9.9'
}


    stages {
        stage('Checkout') {
            steps {
                git credentialsId: 'GitHub_Jay', url: 'https://github.com/JamieJay1/spring-petclinic-microservices.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }

    post {
        success {
            echo 'Build and tests completed successfully!'
        }
        failure {
            echo 'Build or tests failed.'
        }
    }
}
