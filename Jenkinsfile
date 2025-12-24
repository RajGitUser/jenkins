pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    environment {
        user = Raj
    }
    
    stages {
        stage("Build") {
            steps {
                script{
                    sh """
                        echo "Build"
                        $user
                    """
                }
                
            }
        }
        stage("Test") {
            steps {
                script{
                    sh """
                        echo "Test"
                    """
                }
            }
        }
        stage("Deploy") {
            steps {
                script{
                    sh """
                        echo "Deploy"
                    """
                }
            }
        }
    }
    post {
        always {
            echo 'I will always say Hello again!'
            cleanWs ()
        }
        success {
            echo 'I am from Success'
        }
        failure {
            echo 'i am from Failure'
        }
        
    }
    
}