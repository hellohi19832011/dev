pipeline {
    agent any


    stages {
        stage('Clone Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/hellohi19832011/dev.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build React App') {
            steps {
                sh 'npm run build'
            }
        }
    }

    post {
        success {
            echo 'React build successful 🎉'
        }
        failure {
            echo 'Build failed ❌'
        }
    }
}
