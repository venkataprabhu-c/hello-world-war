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
               
                sh "cp /var/lib/jenkins/workspace/Hello-world-war_Pipeline /opt/apache-tomcat-11.0.14/webapps/"
            }
        }
    }
    }
