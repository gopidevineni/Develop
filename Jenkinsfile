pipeline {
    agent any
    
    options {
        buildDiscarder(logRotator(numToKeepStr: "10", artifactNumToKeepStr: "10"))
    }
    parameters {
        extendedChoice defaultValue: '', description: 'select the modules', descriptionPropertyValue: '', multiSelectDelimiter: ',', name: 'ModuleNames', quoteValue: false, saveJSONParameterToFile: false, type: 'PT_MULTI_SELECT', value: 'module-1,module-2', visibleItemCount: 5
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
