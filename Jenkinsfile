pipeline {
    agent any
    stages {
    
    stage('checkout') {
    checkout scm
        }
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}
