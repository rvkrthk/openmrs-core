node ('MAVEN'){
    stage('SCM'){
        git 'https://github.com/rvkrthk/openmrs-core.git'
    }
    stage('BUILD'){
        sh 'mvn package'
    }
    stage ('POST BUILD'){
        junit '**/TEST-*.xml'
        archive '**/*.war'
    }
}