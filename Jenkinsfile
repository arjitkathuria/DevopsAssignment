pipeline{
    agent any
    tools{
        aven 'Maven'
    }
    stages{
            stage("checkout"){
                steps{
                    sh "echo checkout"
                }
         }
    stage("build"){
        steps{
            sh "mvn clean"
        }
    }
    stage("Unit test"){
        steps{
            sh "mvn test" 
        }
     }
    }
    
    post{
        success{
            sh "echo build is success"
        }
        
    }

}
