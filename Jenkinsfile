pipeline {

    agent any

    triggers {
        pollSCM('*/2 * * * *')
    }

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

    post {

        success {
            archiveArtifacts artifacts: 'target/*.jar'
        }

    }

}