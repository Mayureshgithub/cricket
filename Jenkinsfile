pipeline {
    agent any
    stages {
        stage('Git checkout') {
            steps {
                git credentialsId: 'test', url: 'git@github.com:Mayureshgithub/Mayureshgithub.git'
            }
        }
       stage("Builds"){
            steps {
               sh 'mvn clean package'
            }
         }
    }
}
