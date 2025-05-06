pipeline {

    agent any

    tools {

        maven "maven"
    }

    
    stages {
        stage('Build Maven') {
            steps{
               checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'my-git', url: 'https://github.com/Keerthan778/jenkins-maven_trail.git']])
                sh "mvn -Dmaven.test.failure.ignore=true clean package"
                
            }
        }
    }
    
}
