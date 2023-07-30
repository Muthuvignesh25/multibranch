@Library("sharedlib")_
pipeline{
    agent any
    stages{
        stage('Continuous Download'){
            steps{
                script{
            cicd.gitv("multibranch")
                }
            }
         }
        stage('Continuous Build'){
            steps{
                 script{
               cicd.mavenv()
               
                 }
            }
         }
        stage('Countinuous Deploy'){
            steps{
                 script{
               cicd.deployv("DeclarativePipeline","172.31.15.226","t")
                 }
                   
            }
       
         }
        stage('Continuous Testing'){
            steps{
                 script{
                 cicd.gitv("FunctionalTesting")
                cicd.testv("DeclarativePipeline")
                 }
            }
        }   
    }
    post{
        success{
             script{
            cicd.deployv("DeclarativePipeline","172.31.7.50","p") 
             }
 }
    }
   
}

   
