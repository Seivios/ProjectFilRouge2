pipeline {
    agent any
stages {
stage ('run collection') {
steps {
sh 'docker run -t postman/newman run -h'
sh 'docker run -v run collection-1.json --color off --disable-unicode'
}
}
}
}