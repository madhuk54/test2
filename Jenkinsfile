pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/madhuk54/test2.git'
            }
        }

        stage('Check Files') {
            steps {
                bat 'dir'  
            }
        }

        stage('Compile Java') {
            steps {
                bat 'javac student.java'
            }
        }

        stage('Run Java Program') {
            steps {
                bat 'java Student'
            }
        }
    }

    post {
        success {
            echo 'Pipeline execution completed successfully!'
        }
        failure {
            echo 'Pipeline execution failed!'
        }
    }
}

