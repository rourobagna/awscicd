pipeline {
    agent any
    environment {
        branch_name = 'main'
        GIT_URL = 'https://github.com/rourobagna/awscicd.git'
    }
     stages {
       stage('git checkout'){
        steps{
            git branch: "${BRANCH_NAME}", url: "${GIT_URL}"
        }
       }
       stage('docker build'){
        steps{
            sh 'docker build -t awscicd .'
            sh 'docker images'
        }
       }
    } 
}