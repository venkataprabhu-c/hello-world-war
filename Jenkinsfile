pipeline {
    // agent { label 'java' }
    agent none
    stages {
        stage('hello-world-war') {
        parallel {
        stage('checkout') {
            agent { label 'java' }
             steps {
               sh "rm -rf hello-world-war"
               sh "git clone https://github.com/venkataprabhu-c/hello-world-war.git"
           }
        }
        stage('Build') {
            agent { label 'java' }
             steps {
               sh "mvn clean package"
           }
        }
        
        stage('Deploy') {
            agent { label 'java' }
             steps {
               sh "sudo cp /home/slave1/workspace/Hello-world-war_Pipeline/target/hello-world-war-1.0.0.war /opt/apache-tomcat-11.0.14/webapps/"
           }
        }
    }
}
        }
        }
