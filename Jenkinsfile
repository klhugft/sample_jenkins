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
                    extendedChoice multiSelectDelimiter: ',', name: 'vendorTypeList', propertyFile: '/Users/klhu/Desktop/test/test.properties', propertyKey: 'prop1', quoteValue: false, saveJSONParameterToFile: false, type: 'PT_CHECKBOX', visibleItemCount: 5
                    
                }

                

            }
            steps {
                echo 'choice is ...'
            }
        }
        

        stage('Parameters'){
                steps {
                    script {
                    properties([
                            parameters([
                                [$class: 'WHideParameterDefinition', 
                                    name: 'HIDDEN_PARAM', 
                                    description: 'Select the Environemnt from the Dropdown List', 
                                    filterLength: 1, 
                                    filterable: false, 
                                    script: [
                                        $class: 'GroovyScript', 
                                        fallbackScript: [
                                            classpath: [], 
                                            sandbox: false, 
                                            script: 
                                                "return['Could not get The environemnts']"
                                        ], 
                                        script: [
                                            classpath: [], 
                                            sandbox: false, 
                                            script: 
                                                "return['dev','stage','prod']"
                                        ]
                                    ]
                                ]
                            ])
                    ])
                    }
                }
        
        }
    }
}




