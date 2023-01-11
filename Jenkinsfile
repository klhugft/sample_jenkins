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
            feed_list = [a,b,c,d]
            input {
                message "Let's promote?"
                ok 'Choose'
                
                parameters {
                    extendedChoice choices: feed_list, description: '', descriptionPropertyValue: 'blue,green,yellow,blue', multiSelectDelimiter: ',', name: 'favColor', quoteValue: false, saveJSONParameterToFile: false, type: 'PT_CHECKBOX', value: 'blue,green,yellow,blue', visibleItemCount: 5
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