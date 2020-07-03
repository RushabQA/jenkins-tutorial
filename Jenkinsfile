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
                    sh "sudo curl -L https://github.com/docker/compose/releases/download/1.26.1/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose"
                }
            }   
            stage('Deploy'){
                steps{
                    sh "sudo docker-compose up -d"
                }
            }
}

        
        
        
