pipeline {
    agent any
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
                tar -cvf $JOB_BASE_NAME-$BUILD_ID.tar **/**.war 
                '''    
            }
         }
    }
}
