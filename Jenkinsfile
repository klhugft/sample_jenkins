pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        
        stage('Example') {
            input {
                message "Let's promote?"
                ok 'Choose'
                parameters {
                    multipleChoice(name: 'Environments', choices: ["prod", "eu", "test", "mgmt"], description: 'Environments to create parameter in'),
                string(name: 'Path', description: 'SSM Parameter Path'),
                text(name: 'Value', description: 'Parameter Value')
                }
            }    
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying....'
        
            }
        }
    }
}