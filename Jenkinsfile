pipeline {
    agent { label 'linux-node' }   // use your agent node
    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    // Build Docker image using the Dockerfile in repo
                    docker.build('node-webapp-image')
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                script {
                    // Run the container
                    docker.image('node-webapp-image').run('-d -p 3000:3000')
                }
            }
        }
    }
}

