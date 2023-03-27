pipeline {
    agent any
    stages {
    stage('checkout '){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/feat-project2']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/prjpracticeteam/githubpractice.git']]])
            }
        }
        stage('docker image  build') {
            steps {
                sh 'docker build . :jekins_docker'
            }
        }
        stage(' runing program'){
            steps{
                sh ' python main.py L1.txt L2.txt R.txt
            }
        }
    }
}
