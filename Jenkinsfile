pipeline {
    agent {
        label 'slave'
    }
    tools{
        maven 'maven3'
    }
    stages{
        stage('checkout') {
            steps {
                git branch: 'featurs/mohamed_didi', credentialsId: '038b4828-ff35-4a5f-9ad8-b15dc24b648b', url: 'https://github.com/di-amine/Projet_CI-CD.git'
            }
        }
        stage ('Build') {
            steps {
                sh 'mvn deploy'
            }
        }
    }
}

