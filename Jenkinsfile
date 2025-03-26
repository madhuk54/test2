pipeline {
    agent any 
     environment {
        JAVA_HOME = "C:\\Program Files\\Java\\jdk-21"
        PATH = "${JAVA_HOME}\\bin;${env.PATH}"
    }
    stages {
        stage('Clone from GitHub') {
            steps {
                git branch: 'main', url: 'https://github.com/madhuk54/test.git'
            }
        }

        stage('Compile Java') {
            steps {
                bat 'javac student.java' 
            }
        }

        stage('Run Java Program') {
            steps {
                bat 'java student'  
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
