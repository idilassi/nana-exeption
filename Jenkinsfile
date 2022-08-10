CODE_CHANGES = getGitChanges()
pipeline {
    agent any
    stages{
           stage("build") {
            when {
                     expression {
                        BRANCHE_NAME == 'main' && CODE_CHANGES == true
                     }
                }
             steps {
                 echo 'build complete'   
             } 
            }

            stage("test") {
                when {
                     expression {
                        BRANCHE_NAME == 'main'
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



