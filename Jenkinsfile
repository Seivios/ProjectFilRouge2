pipeline {
    agent {
        docker {
            image 'node:lts-bullseye-slim'
            args '-p 3000:3000'
        }
    }
    stages {
        stage('Build') {
            steps{
                sh 'apt-get install -y npm'
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