pipeline {
    agent {
        label 'agent-2'
    } 

    stages {
        stage('build') {
            steps {
                script{
                    sh """
                      echo 'npm install'
                    """
                }
                
            }
        }

        stage('Test') {
            steps {
                script{
                    sh """
                      echo 'npm test'
                    """
                }
                
            }
        }

        stage('Build') {
            steps {
                script{
                    sh """
                      echo 'npm run build'
                    """
                }
                
            }
        }
    }
     post{
        always{
            echo 'I will always say Hello again!'
            cleanWs()
        }
        success {
            echo 'I will run if success'
        }
        failure {
            echo 'I will run if failure'
        }
     }
}