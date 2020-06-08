pipeline {
    agent any
    triggers {
        upstream(upstreamProjects: 'dummy', threshold: hudson.model.Result.SUCCESS)
    }
    stages {
        stage ('scm') {
            steps {
                git 'https://github.com/GitPr-cticeRepo/spring-petclinic.git'
            }
        }
        stage ('build') {
           steps {
                sh 'mvn package'
                input 'continue to next step?'
                archiveArtifacts 'target/*.jar'
           }
        }
        
    }
}