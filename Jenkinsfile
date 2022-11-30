#!groovy

pipeline {
 agent none
 stages {
   stage('Maven Install') {
     agent {
       sudo docker {
         image 'maven:3.5.0'
       }
     }
     steps {
       sh 'mvn clean install'
     }
   }
   stage('sudo Docker Build') {
     agent any
     steps {
       sh 'sudo docker build -t website .'
     }
   }
 }
}
