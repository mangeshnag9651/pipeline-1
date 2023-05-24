pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                echo 'this is my first pipeline'
            }
        }
        stage('Deploy to Remote'){
            steps{
                sshagent(['deploy-user']) {
                sh 'scp -o stricthostkeychecking=no ${WORKSPACE}/* ubuntu@3.83.99.250:/home/ubuntu/var/www/html/'
                    }
            }
        }
    }
}
