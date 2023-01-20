agent any       
    stages {
        stage('Build') {
            steps{
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