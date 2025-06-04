pipeline {
    agent {
        docker {
            image 'roemer/universal-jenkins-agent:latest'
        }
    }

    stages {
        stage('Verify Docker Agent') {
            steps {
                echo "Running basic check inside Docker container..."
                sh 'echo Hello from Docker agent!'
                sh 'python3 --version'
            }
        }
    }
}
