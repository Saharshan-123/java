pipeline {
    agent any

    stages {
        stage('gitjobtest') {
            steps {
                echo 'Cloning..'
              git branch: 'main', url: 'https://github.com/Saharshan-123/java.git'
            }
        }
       stage('buildjobtest') {
            steps {
                echo 'building..'
                sh 'mvn compile'
            }
        }
        stage('testjobtest') {
            steps {
                echo 'testing..'
                sh 'mvn test'
            }
        }
        stage('deployjob') {
            steps {
                echo 'deploying..'
                sh 'mvn install'
            }
        }
    }
}
