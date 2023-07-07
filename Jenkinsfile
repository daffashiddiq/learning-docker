pipeline {
    agent any
    
    stages {
        stage('Cleanup') {
            steps {
                // Add your cleanup actions here
                sh 'rm -rf learning-docker'
            }
        }
        
        stage('Clone') {
            steps {
                // Add your cloning actions here
                git branch: 'main', url: 'https://github.com/daffashiddiq/learning-docker.git'
            }
        }
        
        stage('Build') {
            steps {
                // Add your build actions here
                sh 'go build -o learning-docker'
            }
        }
        
        stage('Test') {
            steps {
                // Add your test actions here
                sh 'go test ./...'
            }
        }
        
        stage('Run') {
            steps {
                // Add your run actions here
                sh './learning-docker'
            }
        }
    }
}
