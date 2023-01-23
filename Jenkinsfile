pipeline {
    agent any
    stages {
        stage('SCM') {
            steps {
                checkout scm
            }
        }
        stage('Docker node test') {
            agent {
                docker{
                    image 'node:lts-bullseye-slim'
                    args '-p 3000:3000'
                }
                    
            }
            steps{
                sh 'yarn add npm'
                sh 'npm install -g newman'
                sh 'newman run newman/ProjetfilRougeCollection.postman_collection.json -e newman/EnvFilRouge.postman_environment.json'
            }
        }
      
        stage('SonarQube Analysis') {
            steps {
                script {
                    def scannerHome = tool 'SonarqubeScanner'
                    withSonarQubeEnv() {
                        sh "${scannerHome}/bin/sonar-scanner"
                    }
                }
            }
        }
    }
}