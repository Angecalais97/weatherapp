pipeline {
    agent any
    
    stages {
        stage('Install Docker') {
            steps {
                script {
                    sh 'command -v docker || (curl -fsSL https://get.docker.com -o get-docker.sh && sudo sh get-docker.sh)'
                }
            }
        }

        stage('Install Docker Compose') {
            steps {
                script {
                    sh 'command -v docker-compose || (sudo curl -L https://github.com/docker/compose/releases/latest/download/docker-compose-Linux-x86_64 -o /usr/local/bin/docker-compose && sudo chmod +x /usr/local/bin/docker-compose)'
                }
            }
        }

        stage('Install jq') {
            steps {
                script {
                    def jqInstalled = sh(script: 'command -v jq', returnStatus: true) == 0
                    if (!jqInstalled) {
                        sh 'sudo apt-get update && sudo apt-get install -y jq'
                    } else {
                        echo "jq is already installed."
                    }
                }
            }
        }
    }
}
