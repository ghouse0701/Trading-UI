pipeline {
    agent any
      

    stages {
        stage('Git checkout') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/ghouse0701/Trading-UI.git'
                   }
}
        stage('Install npm prerequisites'){
            steps{
                sh'npm audit fix --force'
                sh'npm install'
                sh'npm run build'
                sh'cd /var/lib/jenkins/workspace/task6-job/build'
                sh'pm2 --name Trading-UI start npm -- start'
            }
        }
    }
}
