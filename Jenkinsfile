pipeline {
    agent any

    stages {

        stage('checkout') {
            steps {
                deleteDir()
                sh '''
                    git clone https://github.com/fidinjaleel/Company-website-cicd.git
                '''
            }
        }

        stage('deploy') {
            steps {
                sh '''
                    rm -rf /var/www/html/*
                    cp -r Company-website-cicd/* /var/www/html/
                '''
            }
        }
    }
}
