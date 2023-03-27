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
                sh 'docker build -t test:latest .'
            }
        }
        stage(' Runing program '){
            steps{
                 sh ' python3 main.py L1.txt L2.txt R.txt '
            }
        }
    }
}
