pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/SahilBhostekar/java-factorial.git' // Replace with your repo URL
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
                emailext subject: "Jenkins Build Successful",
                    body: "The Jenkins pipeline for the Factorial application has completed successfully.",
                    to: 'bhostekarsahil24@gmail.com'
            }
        }
    }
}
