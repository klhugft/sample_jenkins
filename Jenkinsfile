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
                feed_list = [a,b,c,d]
                parameters {
                    editableChoice choices: feed_list , description: '', multiSelectDelimiter: ',', name: 'favColor', quoteValue: false, saveJSONParameterToFile: false, type: 'PT_CHECKBOX'
                }
            }
            steps {
                echo "Your favorite color is ${favColor}"
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying....'
        
            }
        }
    }
}