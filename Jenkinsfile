pipeline {
    agent any
    stages {
        stage('---clean---') {
            steps {
                sh "${Maven_Home}/bin/mvn clean"
            }
        }
        stage('--test--') {
            steps {
                sh "${Maven_Home}/bin/mvn test"
            }
        }
        stage('--package--') {
            steps {
                sh "${Maven_Home}/bin/mvn package"
            }
        }
        stage('Email Notification') {
            steps{
              mail bcc: '', body: 'Hi team, welcome to jenkins job alerts......', cc: '', from: '', replyTo: '', subject: 'Jenkins job', to: 'agyr12345678@gmail.com'
            }  
        }
    }
}
