pipeline {
    agent any

    tools {
        // These names must match the ones configured in Jenkins > Global Tool Configuration
        jdk 'jdk-21'
        maven 'Maven 3.9.6'
    }
stages {
        stage('Clone Code') {
            steps {
                echo 'Cloning repository...'
                git branch: 'main', url: 'https://github.com/Saharshan-123/java.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Compiling source...'
                sh 'mvn compile'
            }
        }

        stage('Run Tests') {
            steps {
                echo 'Running unit tests...'
                sh 'mvn test'
            }
        }

        stage('Verify & Package') {
            steps {
                echo 'Verifying and packaging application...'
                sh 'mvn verify'
            }
        }

         stage('Deploy') {
            steps {
                 echo 'Deploying...'
                sh 'mvn deploy'
          }
         }


    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
}    
