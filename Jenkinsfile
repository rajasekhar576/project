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
                sh 'mvn sonar:sonar -Dsonar.host.url=http://3.227.1.88:9000 -Dsonar.login=90713b05d3a12916463474479ddb7537d039d1d1'
            }
        }
    }
}
