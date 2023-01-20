pipeline {
    agent {
label 'docker' 
  }
    stages {
stage('Docker node test') {
agent {
docker {
            image 'node:lts-bullseye-slim'
            args '-p 3000:3000'
        }
}
            steps{
                sh 'apt-get update && apt-get install -y npm'
                sh 'npm install'
            }
        }
    }
}
