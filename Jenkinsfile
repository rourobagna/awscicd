pipeline {
    agent any
     stages {
       stage('git checkout'){
        steps{
            git branch: 'main', url: 'https://github.com/rourobagna/awscicd.git'
        }
       }
       stage('test'){
        steps{
            sh 'echo test'
        }
       }
       stage('trigger'){
        steps{
            sh 'echo trigger'
        }
       }
     } 



}