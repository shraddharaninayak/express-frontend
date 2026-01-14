pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/<your-username>/express-frontend.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Restart Express') {
            steps {
                sh 'pm2 restart express-app || pm2 start index.js --name express-app'
            }
        }
    }
}
