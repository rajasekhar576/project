pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('Unit Testing') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Sonar Analysis') {
            steps {
                sh 'mvn sonar:sonar -Dsonar.host.url=http://3.233.219.57:9000 -Dsonar.login=90713b05d3a12916463474479ddb7537d039d1d1'
            }
        }
        stage('Package to Nexus'){
            steps {
                sh 'mvn package'
            }
        }
    }
}
