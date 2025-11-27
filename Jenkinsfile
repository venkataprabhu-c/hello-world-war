pipeline {
    agent { label 'java' }
   
    stages {
        stage('Checkout') {
            steps {
                sh "rm -rf hello-world-war"
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
               
                sh "sudo cp /home/slave1/workspace/Hello-world-war_Pipeline/target/hello-world-war-1.0.0.war /opt/apache-tomcat-11.0.14/webapps/"
            }
        }
    }
    }
