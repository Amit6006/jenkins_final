pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Amit6006/jenkins_final.git'
            }
        }

        stage('Compile') {
            steps {
                bat 'javac Test.java'
            }
        }

        stage('Run') {
            steps {
                bat 'java Test'
            }
        }
    }

    post {
        always {
            cleanWs()
        }
        success {
            echo 'Java program executed successfully!'
        }
        failure {
            echo 'Execution of Java program failed.'
        }
    }
}
