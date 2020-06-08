node ('LINUX') {
    stage ('scm') {
        git 'https://github.com/GitPr-cticeRepo/spring-petclinic.git'
    }
    stage ('build') {
        sh 'mvn package'
    }
}