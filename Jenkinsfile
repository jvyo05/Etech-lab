pipeline{
    agent any
    tools { maven 'maven'}
    stages{
      stage('git-clone'){
        steps{
           checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'git-check', url: 'https://github.com/jvyo05/Etech-lab']]])  
        }
      }
      stage ('etech-hello'){
        steps{
            sh 'git version'
        }
      }
     stage('Build Artifact - Maven') {
      steps {
        sh "mvn clean package -DskipTests=true"
        archive 'target/*.jar'
      }
     }
    }
    
}
