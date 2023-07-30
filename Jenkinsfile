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
       
        stage('Continuous Testing'){
            steps{
                 script{
                 cicd.gitv("FunctionalTesting")
                cicd.testv("DeclarativePipeline")
                 }
            }
        }   
    }
    
   
}

   
