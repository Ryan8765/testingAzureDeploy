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

        stage('deploy') {
            azureWebAppPublish azureCredentialsId: env.AZURE_CRED_ID,
            resourceGroup: env.RES_GROUP, 
            appName: env.WEB_APP, 
            filePath: "**/*.*",
            sourceDirectory: "build"
        }

    }
}