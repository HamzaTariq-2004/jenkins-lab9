pipeline {
    agent  {
        image 'roemer/universal-jenkins-agent:latest'
        args '-v /var/run/docker.sock:/var/run/docker.sock'
    }

    stages {
        stage('Test') {
            steps {
                echo 'Running basic syntax check...'
                sh 'python3 -m py_compile app.py'
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
