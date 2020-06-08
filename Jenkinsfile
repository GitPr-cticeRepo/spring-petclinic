pipeline {
    agent {label 'MASTER'}
    stages {
        stage ('source') {
            steps {
                git 'https://github.com/GitPr-cticeRepo/spring-petclinic.git'
            }
        }
        stage ('build') {
            steps {
                sh 'mvn package'
            }
         
        }
    }
}