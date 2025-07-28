pipeline {
    agent any
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
}
}  
