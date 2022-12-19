pipeline{
    agent{
        label 'saler-node'
    }
    stages{
        stage('clone'){
            steps{
                git url: 'https://github.com/tarunkumarpendem/saleor-platform.git',
                    branch: 'main'
            }
        }
        stage('docker_image_build'){
            steps{
                sh 'docker image build -t tarunkumarpendem/saler:dev .'
                sh 'docker image push tarunkumarpendem/saler:dev'
            }
        }
    } 
}