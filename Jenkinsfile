#!groovy
pipeline {
   agent none
  stages {    
   stage('sudo Maven Install') {
     agent {        
      docker {          
        image 'maven:3.5.0'
    }      
 }      
 steps {
      sh 'mvn clean install'
      }
    }
   }
}
