pipeline {

    agent any

    tools {
        maven 'Maven-3.9'
    }

    stages {

        stage('Compile') {

            steps {
                bat 'mvn compile'
            }

        }

        stage('Test') {

            steps {
                bat 'mvn test'
            }

        }

        stage('Package') {

            steps {
                bat 'mvn package'
            }

        }

    }

}