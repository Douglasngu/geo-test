 pipeline{
    agent any 
    tools{
         maven 'M2_HOME'
    }
    stages{
    stage('maven clean'){
        steps{
        sh  'mvn clean'
        }
    }
    stage('maven install'){
        steps{
          sh  'mvn install'
            
        }
    }
    stage('maven package'){
        steps{
         sh   'mvn package'
        }
    }
   stage('upload artifact'){
        steps{
            sh 'curl --upload-admin:devops -v http://198.58.119.40:8081/repository/Douglas-repo/'
        }
    }

    }

}