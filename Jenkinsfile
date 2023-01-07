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
                    extendedChoice defaultValue: 'blue,green,yellow,blue', description: '', descriptionPropertyValue: 'blue,green,yellow,blue', multiSelectDelimiter: ',', name: 'favColor', quoteValue: false, saveJSONParameterToFile: false, type: 'PT_MULTI_SELECT', value: 'blue,green,yellow,blue', visibleItemCount: 5
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