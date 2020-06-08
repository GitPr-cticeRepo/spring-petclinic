pipeline {
    agent {label 'MASTER'}
    triggers {
        upstream(upstreamProjects: 'dummy', threshold: hudson.model.Result.SUCCESS)
    }
    parameters {
        string(name: 'BRANCH_FOR_BUILD', defaultValue: 'master', description: 'Enter the branch to build')
    }
    stages {
        stage ('Source') {
            steps {
                git url: 'https://github.com/GitPr-cticeRepo/spring-petclinic.git', branch: "${params.BRANCH_FOR_BUILD}"
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