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
      }
   
}

   
