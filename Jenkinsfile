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
                sh 'scp -r stricthostkeychecking=no ${WORKSPACE}/* ubuntu@3.83.99.250:/var/www/html/'
                    }
        }
    }
}
