pipeline {
    agent any
    stages {

        stage('Install Dependencies') {
            steps {
                bat'npm install'
            }
        }

        stage('Build the Project') {
            steps {
                bat'npm run build'
            }
        }



    }
}