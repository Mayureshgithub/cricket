pipeline {
    agent any
    enviornment{
    PATH = "/opt/apache-maven-3.8.6/bin:$PATH"
    }
 stages {
        stage('Git checkout') {
            steps {
                git credentialsId: 'test', url: 'git@github.com:Mayureshgithub/Mayureshgithub.git'
            }
        }
       stage("Build"){
            steps {
                sh '''
                mvn clean package
               
                '''    
            }
         }
    }
}
