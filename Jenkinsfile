pipeline {
    agent { label "Slave"}
    stages{
        stage('checkout'){
        steps{
            git "git@github.com:dbricker-intel/sela-devops-courses-jenkins-cicd-demo-app.git"
        }
        }
        stage('install'){
        steps {
            sh 'npm install'
        }
        }
        stage('test'){
        steps{
            sh 'npm run test'
        }
        }
        stage('package'){
        steps{
            sh 'npm run build'
        }
        }
        stage('Archive'){
        steps{
            archiveArtifacts '*.zip'
        }
        }
    }
    
}
