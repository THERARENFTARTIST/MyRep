pipeline {
    agent any

    stages {
        stage('#1.Checkout') {
            steps {
                git 'https://github.com/THERARENFTARTIST/MyRep'
            }
        }

        stage('#2.Build the image') {
            steps {
                bat 'docker build -t mywebsite .'
            }
        }
        stage('#3.Stop all old containers'){
            steps{
                bat 'docker stop mycont || exit 0'
                bat 'docker rm mycont || exit 0'
            }
        }
        stage('#4.Run the image - Containerize'){
            steps{
                bat 'docker run -d -p 4001:80 --name mycont mywebsite'
            }
        }
    }
}
