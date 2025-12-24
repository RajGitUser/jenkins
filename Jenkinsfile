pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    
    stages {
        stage("Build") {
            steps {
                echo "Build"
            }
        }
        stage("Test") {
            steps {
                echo "Test"
            }
        }
        stage("Deploy") {
            steps {
                echo "Deploy"
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