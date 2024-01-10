pipeline {
    agent any
    tools {
      maven 'maven'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/rajesh-31/hello-world.git']])
              
            }
        }

        stage('Build') {
            steps {
                echo "compile the code"
                sh 'mvn compile'
               
            }
        }

        
    }

    post {
        success {
            echo 'Pipeline successfully ran!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
