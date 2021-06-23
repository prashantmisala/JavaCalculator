pipeline {
    agent any
    stages {
        stage('compile') { 
            steps {
            echo 'compile'
            sh 'mvn compile'
            }
        }
        stage('package') { 
            steps {
            echo 'package'
            sh 'mvn package'
            }
        }
        stage('testing') {
            steps {
            echo 'package'
            sh 'mvn sonar:sonar -Dsonar.host.url=http://54.157.123.2:9000 -Dsonar.login=d5d588ba2c8d39d399f49fa07207018595b16e3d'
            }
       }
       stage('deploy') {
            steps {
            sh 'mvn deploy'
            }
        }
    }    
 }  
     
    

