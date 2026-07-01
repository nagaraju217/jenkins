pipeline {
    agent {
        label 'agent-2'
    } 
    environment{
        COURSE="Jenkins"
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

        stage('get users') {
            steps {
                script{
                    sh """
                      cat /etc/passwd
                      echo "$COURSE"
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