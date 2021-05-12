pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                ws('repo'){
                    git credentialsId: 'git_credentials', url: 'https://gitlab-talentboost.vmware.com/stanislavhristov00/utms-sandbox.git'
                }
            }
        }

        stage('Copy artifact'){
            steps {
                copyArtifacts(projectName: 'utms-cli');
            }
        }

        stage('Run tests'){
            steps{
                sh 'java -jar **/utms-cli.jar --config /var/lib/jenkins/workspace/UTMS/utms-sandbox/testing.yaml --server http://localhost:8081/api -d'
            }
        }
    }
}