pipeline {
    agent any
   
    stages {
        stage('Checkout') {
            steps {
                    sh "git clone https://github.com/venkataprabhu-c/hello-world-war/"
            }
        } 
         stage('Build') {
            steps {
                sh "mvn clean package"
            }
        }   
        stage('Deploy') {
            steps {
                sh "cp /var/lib/jenkins/workspace/hello-world-war-1.0.0.war /opt/apache-tomcat-11.0.14/webapps/"
            }
        }
    }
    }
