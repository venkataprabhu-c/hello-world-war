pipeline {
    // agent { label 'java' }
    agent none
    parameters {
string(name: 'mcmd', defaultValue: 'clean', description: 'Maven clean')
booleanParam(name: 'SAMPLE_BOOLEAN', defaultValue: true, description: 'A boolean parameter')
choice(name: 'mcmd1', choices: ['validate','compile', 'package','install'], description: 'Choose one option')
}
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
               sh "mvn $mcmd mcmd1"
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
