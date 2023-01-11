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
                    extendedChoice multiSelectDelimiter: ',', propertyFile: 'test.properties' name: 'lets try', quoteValue: false, saveJSONParameterToFile: false, type: 'PT_CHECKBOX'
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