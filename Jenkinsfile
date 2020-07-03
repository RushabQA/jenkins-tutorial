pipeline{
        agent any
        stages{
            stage('Clone GIT Repo'){
                steps{
                    sh "git clone https://gitlab.com/qacdevops/chaperootodo_client.git"
                }
            }
            stage('Install Docker'){
                steps{
                    sh "curl https://get.docker.com | sudo bash"
                }
            }
            stage('Install Docker Compose'){
                steps{
                    sh "curl -s https://api.github.com/repos/docker/compose/releases/latest | jq -r '.tag_name' | sudo bash"
                }
            }   
            stage('Deploy'){
                steps{
                    sh "sudo docker-compose up -d"
                }
            }
}

        
        
        
