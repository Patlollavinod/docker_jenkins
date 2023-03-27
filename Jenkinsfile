pipeline {
    agent any
    stages {
    stage('checkout '){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Patlollavinod/docker_jenkins.git']]])
            }
        }
        stage('docker image  build') {
            steps {
                sh 'docker build . :jekins_docker'
            }
        }
        stage(' Runing program '){
            steps{
                 git branch: 'main', url: 'https://github.com/Patlollavinod/docker_jenkins.git'
                 sh ' python main.py L1.txt L2.txt R.txt '
            }
        }
    }
}
