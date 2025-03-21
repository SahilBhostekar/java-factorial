pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/SahilBhostekar/java-factorial.git'
            }
        }

        stage('Build') {
            steps {
                sh 'javac Factorial.java'
            }
        }

        stage('Run Application') {
            steps {
                sh 'java Factorial'
            }
        }

        stage('Post Build Notification') {
            steps {
                mail to: 'your-2024.sahil.bhostekar@ves.ac.in',
                     subject: "Build Successful",
                     body: "The Jenkins pipeline build was successful."
            }
        }
    }
}
