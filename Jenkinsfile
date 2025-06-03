pipeline {
    agent { label 'docker-agent' }

    stages {
        stage('Test') {
            steps {
                echo 'Running basic syntax check...'
                sh 'python3 -m py_comile app.py'
            }
        }
        stage('Build') {
            steps {
                echo 'Building Docker image...'
                sh 'docker build -t hamza/test-pipeline-app .'
            }
        }
        stage('Deploy') {
            steps {
            echo 'Running Docker container...'
            sh 'docker run --rm hamza/test-pipeline-app'
            }
        }
    }
}
