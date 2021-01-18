pipeline{
    agent any
    stages{
            stage("checkout"){
                steps{
                    sh "echo checkout"
                }
         }
    stage("build"){
        steps{
            sh "echo build"
        }
    }
    stage("Unit test"){
        steps{
            sh "echo unit test" 
        }
     }
    }
    
    post{
        success{
            sh "echo build is success"
        }
        
    }

}
