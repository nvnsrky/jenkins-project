pipeline {
    agent any
    
    stages {
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
