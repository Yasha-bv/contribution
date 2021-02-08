pipeline {
    agent any
    stages {
        stage('---clean---') {
            steps {
                sh "C:/maven/apache-maven-3.6.3/bin/mvn clean"
            }
        }
        stage('--test--') {
            steps {
                sh "C:/maven/apache-maven-3.6.3/bin/mvn test"
            }
        }
        stage('--package--') {
            steps {
                sh "C:/maven/apache-maven-3.6.3/bin/mvn package"
            }
        }
        stage('Email Notification') {
            steps{
              mail bcc: '', body: 'Hi team, welcome to jenkins job alerts......', cc: '', from: '', replyTo: '', subject: 'Jenkins job', to: 'agyr12345678@gmail.com'
            }  
        }
    }
}
