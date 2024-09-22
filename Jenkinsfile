pipeline {
    agent any
    environment {
        branch_name = 'main'
        GIT_URL = 'https://github.com/rourobagna/awscicd.git'
        IMAGE_TAG = 'rourobagna/awscicd'
        IMAGE_VERSION = ${BUILD_NUMBER}
    }
     stages {
       stage('git checkout'){
        steps{
            git branch: "${BRANCH_NAME}", url: "${GIT_URL}"
        }
       }
       stage('docker build'){
        steps{
            sh 'docker build -t "${IMAGE_TAG}:${IMAGE_VERSION}" .'
            sh 'docker images'
        }
       }
    } 
}