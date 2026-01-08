pipeline {
  agent any
  tools{
    maven: 'Maven 3.9.6'
  }
    stages {
      stage('Build') {
      steps {
      echo 'compiling syfoo app.....'
      sh 'mvn compile'
      }
    }
      stage('Test') {
      steps {
        echo 'testing syfoo app.....'
      sh 'mvn clean test'
      }
    }
      stage('Package') {
      steps {
        echo 'packaging syfoo app.....'
      sh 'mvn package -DskipTests'
      }
    }
      Post{
      always{
        echo 'this pipeline is completed....'
      }
    }
  }
