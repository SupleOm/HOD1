pipeline {
       agent any
                 
       stages{
            stage('Checkout') {
               steps {
                      checkout scm
                     } }
            stage('build'){
               steps{ 
                  mvn install
                     } }
            stage('deploy'){
               steps{
                  cp target/HOD1.war /home/omsuple/Devopstool/apache-tomcat-9.0.93/webapps
                     } }
                  }
        }             
