pipeline {
       agent any
                 
       stages{
            stage('Checkout') {
               steps {
                      checkout scm
                     } }
            stage('build'){
               steps{ 
                 sh 'mvn install'
                     } }
            stage('deploy'){
               steps{
                 sh  'cp target/HOD1.war /home/omsuple/Devopstool/apache-tomcat-9.0.93/webapps'
                     } }
                  }
        }             
