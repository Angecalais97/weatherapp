pipeline {
    agent any
    
    stages {
        stage('Install Docker and Tools') {
            steps {
                script {
                    // Download Docker installation script
                    sh 'curl -fsSL https://get.docker.com -o get-docker.sh'
                    
                    // Modify the Docker installation script to avoid sudo for package management
                    sh "sed -i 's/sudo //g' get-docker.sh"
                    
                    // Execute modified Docker installation script
                    sh 'sh get-docker.sh'
                    
                    // Install Docker Compose
                    sh 'curl -L https://github.com/docker/compose/releases/latest/download/docker-compose-Linux-x86_64 -o docker-compose && chmod +x docker-compose && sudo mv docker-compose /usr/local/bin/'
                    
                    // Install jq
                    sh 'sudo apt-get update && sudo apt-get install -y jq'
                }
            }
        }
    }
}
