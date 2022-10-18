pipeline {
    agent any
    tools {maven "maven"} 
      stages {
          stage('Checkout Source'){
              steps{
                deleteDir()
                checkout scm
              }
          }
          
          stage('java build'){
              steps{
                sh "mvn install"
                sh "cd target/ && java -jar *.jar &"
              }
          }

      }
}