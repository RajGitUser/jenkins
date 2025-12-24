pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    environment {
        USER = "Raj"
    }
    options {
        disableConcurrentBuilds ()
    }

    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    
    stages {
        stage("Build") {
            steps {
                script{
                    sh """
                        // echo "Build"
                        // echo $USER
                        // echo "Hello ${params.PERSON}"
                        // echo "Biography: ${params.BIOGRAPHY}"
                        // echo "Toggle: ${params.TOGGLE}"
                        // echo "Choice: ${params.CHOICE}"
                        // echo "Password: ${params.PASSWORD}"
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