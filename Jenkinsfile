pipeline {
    agent any
      
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
                // sh "npm install --force"
                sh "cd target/ && java -jar *.jar"
              }
          }

      }
}