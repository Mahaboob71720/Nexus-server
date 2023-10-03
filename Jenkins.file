@Library('my_shared_libraries') _

pipeline {
    agent any
    
     tools{
         maven "Maven-3.9.4"
        }

    stages {
        stage('Clone'){
            steps {
                git branch: 'main', credentialsId: 'Git-Credentials', url: 'https://github.com/Mahaboob71720/GitHub-Task.git'
            }
        }
        stage('Maven Build'){
            steps{
               mavenBuild()
            }
        }
        stage('Code Review'){
            steps{
                sonarQube()
            }
        }
    }
}
