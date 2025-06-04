pipeline {
    agent {
        docker {
            image 'roemer/universal-jenkins-agent:latest'
        }
    }

    stages {
        stage('Verify Docker Agent') {
            steps {
                echo "Running inside Docker container"
                sh 'whoami'
                sh 'python3 --version'
            }
        }
    }
}
