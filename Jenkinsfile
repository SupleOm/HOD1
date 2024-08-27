pipeline {
       agent any

parameters {
  choice choices: ['DEV', 'QA', 'UAT'], name: 'ENVIRONMENT'
}
                 
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
                script {
			 if ( env.ENVIRONMENT == 'QA' ){
        	sh 'cp target/HOD1.war /home/omsuple/Devopstool/apache-tomcat-9.0.93/webapps'
        	echo "deployment has been COMPLETED on QA!"
			 }
			else ( env.ENVIRONMENT == 'UAT' ){
    		sh 'cp target/HOD1.war /home/swapnil/Documents/DevOps-Software/apache-tomcat-9.0.79/webapps'
    		echo "deployment has been done on UAT!"
			}
			}}}	
}}
                              
