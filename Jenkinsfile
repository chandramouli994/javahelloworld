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
                sh 'cp -rf /root/.jenkins/workspace/helloworld_example/target/helloworld-1.1.jar /tmp/'
                 echo "Copied file successfully"
                 sh 'cd /tmp/'
                 sh 'chmod 777 /tmp/helloworld-1.1.jar'
                 echo "Permission changed successfully"
                 sh 'java -jar /tmp/helloworld-1.1.jar --port=8181'
                 echo "Running Java Application"
            }
            
            }
        }
    }
}
