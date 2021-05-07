pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git credentialsId: 'git_credentials', url: 'https://gitlab-talentboost.vmware.com/stanislavhristov00/utms-sandbox.git'
            }
        }

        stage('Copy artifact'){
            steps {
                copyArtifacts(projectName: 'utms-cli');
            }
        }
    }
}