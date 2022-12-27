pipeline{
    agent{
        label 'node-1'
    }
    stages{
        stage('clone'){
            steps{
                git url: 'https://github.com/tarunkumarpendem/saleor-dashboard.git',
                    branch: 'dev'
            }
        }
        stage('docker_image_build'){
            steps{
                sh """
                      docker image build -t saleor-dashboard:dev .
                      docker image tag saleor-dashboard:dev tarunkumarpendem/saleor-dashboard:dev
                      docker image push tarunkumarpendem/saleor-dashboard:dev
                    """  
            }
        }
    } 
}