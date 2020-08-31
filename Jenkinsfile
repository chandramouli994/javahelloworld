pipeline {
    agent any
    stages {
    
    stage('checkout') { 
        steps {
    checkout scm
        }
    }
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
        stage('Running'){
             steps {
                sh 'cd /root/.jenkins/workspace/helloworld_example/target/'
                 echo "Copied file successfully"
                 sh 'java -jar helloworld-1.1.jar --port=8181'
                 echo "Running Java Application"
            }
            
            }
        }
    }
