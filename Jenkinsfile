pipeline {
    agent any
    
    stages {
        stage('Install Docker and Tools') {
            steps {
                script {
                    // Install Docker
                    sh 'curl -fsSL https://get.docker.com -o get-docker.sh && sudo sh get-docker.sh'
                    
                    // Install Docker Compose
                    sh 'sudo curl -L https://github.com/docker/compose/releases/latest/download/docker-compose-Linux-x86_64 -o /usr/local/bin/docker-compose && sudo chmod +x /usr/local/bin/docker-compose'
                    
                    // Install jq
                    sh 'sudo apt-get update && sudo apt-get install -y jq'
                }
            }
        }
    }
}
