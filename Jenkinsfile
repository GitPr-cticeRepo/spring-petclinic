pipeline {
    agent any
    triggers {
        upstream (upstreamProjects: 'dummy', threshold: hudsom.model.Result.SUCCESS)
    }
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