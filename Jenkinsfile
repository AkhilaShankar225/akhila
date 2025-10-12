pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/AkhilaShankar225/akhila.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                echo 'Installing dependencies...'
                sh 'sudo apt update -y'
                sh 'sudo apt install -y python3 python3-pip'
            }
        }

        stage('Run Script') {
            steps {
                echo 'Running Python script...'
                sh 'python3 testing.py'
            }
        }
    }
}

