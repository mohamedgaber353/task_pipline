pipeline {
    agent any

    stages {
         stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/mohamedgaber353/task_pipline.git'
            }
        }
        stage('Run Script') {
            steps {
                script {
                 sh  'chmod +x ./hello.sh'
                 sh  './hello.sh'
                }
            }
        }

    }
    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
