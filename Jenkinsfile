pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Clones the repository
                git 'https://github.com/THERARENFTARTIST/MyRep.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Compiling in Progress'
                // Compiles the Java file on Windows (bat)
                bat 'javac Hello1.java'
            }
        }

        stage('Execute') {
            steps {
                echo 'Executing...'
                // Runs the compiled Java class
                bat 'java Hello1'
            }
        }
    }
}
