pipeline{
    agent{
        label 'saler-node'
    }
    stages{
        stage('clone'){
            steps{
                git url: 'https://github.com/tarunkumarpendem/saleor-dashboard.git',
                    branch: 'main'
            }
        }
        stage('docker_image_build'){
            steps{
                sh 'docker image build -t saleor:dev .'
                //sh 'docker image push tarunkumarpendem/saleor:dev'
            }
        }
    } 
}