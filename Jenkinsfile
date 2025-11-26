pipeline {
    agent any
   
    stages {
        stage('Checkout') {
            steps {
                sh "rm -rf hello-world-war"
                sh "git clone https://github.com/venkataprabhu-c/hello-world-war/"
            }
        }
    }
}
