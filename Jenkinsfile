pipeline {
    agent any
    tools {
        maven 'maven3'         
    }
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
              echo "mvn clean install"
          }     
      }
   }
}
