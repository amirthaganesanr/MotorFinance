pipeline {
    agent any 
    stages {
        stage('Checkout') { 
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                sh '''npm install
                npm run build'''
            }
        }
       stage('Deploy') {
            steps {
                sh "cp -r $workspace/bundle /opt/apache-tomcat-8.5.37/webapps/"
            }
        }
    }
}