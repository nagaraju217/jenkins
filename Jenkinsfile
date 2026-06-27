pipeline {
    agent {
        label 'agent-1'
    } 

    stages {
        stage('build') {
            steps {
                echo 'npm install'
            }
        }

        stage('Test') {
            steps {
                echo 'npm test'
            }
        }

        stage('Build') {
            steps {
                echo 'npm run build'
            }
        }
    }
}