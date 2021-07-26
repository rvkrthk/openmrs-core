node ('MAVEN'){
    stage('SCM'){
        git 'https://github.com/rvkrthk/openmrs-core.git'
    }
    stage('BUILD'){
        sh 'mvn package'
    }
    postbuild{
        junit '**/TEST-*.xml'
        archive '**/*.war'
    }
}