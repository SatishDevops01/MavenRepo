pipeline {
    agent any
    
    stages {
      stage('SCM Chekout'){
          steps {
             echo 'Code checkout from GIT SCM'
             git credentialsId: 'GitSSHKey', url: 'https://github.com/SatishDevops01/MavenRepo'
          }
      }
      stage('Build Package'){
          steps {
              def mvnHome= tool name: 'maven3', type: 'maven'
              echo 'Build the packages using Maven'
              bat "${mvnHome}/bin/mvn clean install"
          }     
      }
   }
}
