pipeline {
    agent any
    
    stages {
        stage('Install Docker and Tools') {
            steps {
                script {
                    // Install Docker
                    sh 'curl -fsSL https://get.docker.com -o get-docker.sh'
                    sh 'sh get-docker.sh'
                    
                    // Install Docker Compose
                    sh 'sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose'
                    sh 'sudo chmod +x /usr/local/bin/docker-compose'
                    
                    // Install jq
                    sh 'sudo apt-get update && sudo apt-get install -y jq'
                }
            }
        }
    }
}
