pipeline{
    agent any
    stages{
      stage('git-clone'){
            steps{
           checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'git-check', url: 'https://github.com/jvyo05/Etech-lab']]])  
            }
        }
    }
}
