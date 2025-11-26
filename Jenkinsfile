pipeline {
    agent any
   
    stages {
        stage('Checkout') {
            steps {
                sh "rm -rf hello-world-war"
                sh "git clone https://github.com/venkataprabhu-c/hello-world-war/"
            }
        }
    
    stages {
        stage('Build') {
            steps {
                sh "mvn clean package"
            }
        }
    
stages {
        stage('Deploy') {
            steps {
                sh "cp hello-world-war-1.0.0.war /opt/apache-tomcat-11.0.14/webapps/"
            }
        }
    }
    }
    }
}
