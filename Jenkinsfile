pipeline{
    agent any
    tools{
        maven 'Maven'
    }
    stages{
            stage("checkout"){
                steps{
                    sh "echo checkout"
                }
         }
    stage("build"){
        steps{
              sh "export MAVEN_HOME=/Users/arjitkathuria/Desktop/apache-maven-3.6.3"
              sh "export PATH=$PATH:$MAVEN_HOME/bin"
              sh "mvn --version"
              sh "mvn clean package"
              sh "mvn clean"
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
