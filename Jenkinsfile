pipeline{
    agent any

    tools {
         maven 'maven'
    }

    stages{
        stage('checkout'){
            steps{
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: '40fa34c9-455a-481b-8457-1a7236f361ed', url: 'https://github.com/sthaka/java-hello-world-with-maven']])
            }
        }
        stage('build'){
            steps{
               bat 'mvn package'
            }
        }
    }
}
