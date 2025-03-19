pipeline {
    agent any

    stages {
        stage('Clone Code') {
            steps {
                git url: 'https://github.com/Deepak360-A/my-simple-website.git', branch: 'master'
            }
        }

        stage('Deploy to Apache') {
            steps {
                sh 'sudo cp -r * /var/www/html/'
                sh 'sudo systemctl restart apache2'
            }
        }
    }
}
