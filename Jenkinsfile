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
                sh "echo build"
        }
    }
    stage("Unit test"){
        steps{
            sh "echo unit test"
        }
     }
        stage("upload to artifacts"){
            steps{
                sh "export MAVEN_HOME=/Users/arjitkathuria/Desktop/apache-maven-3.6.3"
                 sh "export PATH=$PATH:$MAVEN_HOME/bin"
                rtMavenDeployer{
                    id: 'deployer',
                     serverId: '123456789@artifactory',
                     releaseRepo: 'arjitkathuria.napqa'
                     snapshotRepo: 'arjitkathuria.nagpqa'
                }
                rtMavenRun{
                    pom: 'pom.xml',
                     goals: 'clean install'
                    deployerId: 'deployer'
                }
                rtPublisherBuildInfo{
                    serverId:  '123456789@artifactory',
                }
            }
        }
    }
    
    post{
        success{
            sh "echo build is success"
        }
        
    }

}
