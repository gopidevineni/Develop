pipeline {
    agent any
    parameters {
        extendedChoice defaultValue: '', discription: 'select the modules', discriptionProperyValues: '', multiSelectDelimiter: ',', name: 'modulenames', quoteValue: false, saveJSONParameterToFile: False, type: 'PT_MULTI_SELECT', value: 'module-1,module-2', visibleItemCoun: 20
    }
    stages {
        stage ('Compile Stage') {

            steps {
               
                    sh 'mvn clean compile'
                    echo 'maven clean completed'
            }
        }

        stage ('Testing Stage') {

            steps {
                
                    sh 'mvn test'
                    echo 'mvn test completed'
            }
        }


        //   stage ('Deployment Stage') {
        //      steps {
               
        //              sh 'mvn deploy'
        //              echo 'mvn deploy completed'
                
        //      }
        //  }
     }
 }