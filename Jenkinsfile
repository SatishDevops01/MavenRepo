pipeline {
    agent any
    cat mvnHome= tool name: 'maven3', type: 'maven'
    stages {
      stage('SCM Chekout'){
          steps {
             echo 'Code checkout from GIT SCM'
             git credentialsId: 'GitSSHKey', url: 'https://github.com/SatishDevops01/MavenRepo'
          }
      }
      stage('Build Package'){
          steps {
              echo 'Build the packages using Maven'
              cmd "${mvnHome}/bin/mvn clean install"
          }     
      }
   }
}
