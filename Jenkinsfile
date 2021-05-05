pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git credentialsId: 'git_credentials', url: 'https://gitlab-talentboost.vmware.com/stanislavhristov00/utms-sandbox.git'
            }
        }
        stage('gitlab') {
          steps {
             echo 'Notify GitLab'
             updateGitlabCommitStatus name: 'build', state: 'pending'
             updateGitlabCommitStatus name: 'build', state: 'success'
        }
    }
}