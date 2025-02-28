pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                script {
                    checkout([
                        $class: 'GitSCM',
                        branches: [[name: '*/main']], // Ensure you use the correct branch
                        userRemoteConfigs: [[url: 'https://github.com/mahi504020/hello.git']]
                    ])
                }
            }
        }

        stage('Build') {
            steps {
                echo "Building project..."
                sh 'echo Build step executed'
            }
        }

        stage('Run') {
            steps {
                echo "Running the project..."
            }
        }
    }
}
