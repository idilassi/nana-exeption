pipeline {
    agent any
    stages{
           stage("build") {
             steps {
                 echo 'build complete'   
             } 
            }

            stage("test") {
                when {
                     expression {
                        BRANCHE_NAME == 'master' || BRANCHE_NAME == 'main'
                     }
                }
              steps {
                echo 'test complete'
              }  
            }
            stage("deploy") {
               steps{
                echo 'deploy complete'
               } 
            }
    }    

   
    }
