pipeline {
    agent any
stages {
stage ('run collection') {
steps {
sh 'docker run -t postman/newman run -h'
sh 'docker run -v ${WORKSPACE}:~/filrouge2/git@github.com:Seivios/ProjectFilRouge2.git/ProjectFilRouge2/newman --wordir ~/filrouge2/git@github.com:Seivios/ProjectFilRouge2.git/ProjectFilRouge2/newman -t postman/newman run collection-1.json --color off --disable-unicode'
}
}
}
}