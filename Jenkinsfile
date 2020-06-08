pipeline {
    agant {label 'MASTER'}
    stages {
        stage ('scm') {
            steps {
                git 'https://github.com/GitPr-cticeRepo/spring-petclinic.git'
            }
        }
        stage ('build') {
            sh 'mvn package'
        }
    }
}