pipeline {
    agent {label 'MASTER'}
    triggers { pollscm('* * * * *')}
    stages {
        stage ('clone and compile') {
            steps {
                git branch: 'declarative'
                url: https://github.com/GitPr-cticeRepo/spring-petclinic.git
                sh 'mvn compile'
            }
        }
        
    }
}