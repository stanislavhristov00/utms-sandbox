pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git credentialsId: 'git_credentials', url: 'https://gitlab-talentboost.vmware.com/stanislavhristov00/utms-sandbox.git'
            }
        }
    }
}