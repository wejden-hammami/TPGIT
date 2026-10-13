pipeline {
    agent any
    stages {
        stage('Checkout code') {
            steps {
                git branch: 'master', url: 'https://github.com/wejden-hammami/TPGIT.git'
            }
        }
        stage('Compile code') {
            steps {
                sh 'mkdir -p out'
                sh 'javac -d out src/application/Test.java'
            }
        }
        stage('Execute code') {
            steps {
                sh 'java -cp out application.Test'
            }
        }
        stage('Display message') {
            steps {
                sh 'echo "Hello from github"'
            }
        }
    }
}
