pipeline {
    agent any

    tools {
        maven 'Maven 3.9.6'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Compiling syfoo app...'
                sh 'mvn compile'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing syfoo app...'
                sh 'mvn clean test'
            }
        }

        stage('Package') {
            steps {
                echo 'Packaging syfoo app...'
                sh 'mvn package -DskipTests'
            }
        }
    }

    post {
        always {
            echo 'This pipeline is completed.'
        }
    }
}
