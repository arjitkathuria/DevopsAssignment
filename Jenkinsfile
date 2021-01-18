pipeline{
    agent any
    tools{
        maven 'Maven'
    }
    stages{
            stage("checkout"){
                steps{
                    sh "echo checkout"
                    sh "export MAVEN_HOME=/Users/arjitkathuria/Desktop/apache-maven-3.6.3"
                    sh "export PATH=$PATH:$MAVEN_HOME/bin"
                    sh "mvn --version"
                    sh "mvn clean package"
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
