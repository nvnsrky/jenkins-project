pipeline {
    agent any
    
    stages {
        stage('Install Docker') {
            steps {
                script {
                    sh 'curl -fsSL https://get.docker.com -o get-docker.sh'
                    sh 'sh get-docker.sh'
                }
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build("my-custom-image:latest", "-f /path/to/your/dockerfile/Dockerfile .")
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                script {
                    docker.image("my-custom-image:latest").run("-d -p 8081:8081 --name my-container")
                }
            }
        }
    }
}


