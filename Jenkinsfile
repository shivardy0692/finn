pipeline {
    agent any
    
    tools{
        maven "MAVEN"
    }

    stages {
        stage('SCM') {
            steps {
                git branch: 'release', credentialsId: '81954f28-25df-4d1b-bbe5-f7d31f518a2e', url: 'https://github.com/shivardy0692/finn.git'
            }
        }
        
        stage('Maven Build') {
            steps {
                sh "mvn clean package"
            }
        }
    }
}
