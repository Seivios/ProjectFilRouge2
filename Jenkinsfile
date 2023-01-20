pipeline {
    agent any
    stages {
        stage('Build') {
            steps{
                sh 'sudo apt-get update && apt-get install -y npm'
                sh 'npm install'
            }
        }
        stage('Run Newman tests') {
            steps {
                sh 'npm install -g newman'
                sh 'newman run mycollection.json -e myenvironment.json'
            }
        }
    }
}