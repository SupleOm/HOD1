pipeline {
       agent any

parameters {
  string defaultValue: 'QA', description: '''DEV
QA
UAT''', name: 'ENVIRONMENT'
}

                 
      stages{
            stage('Checkout') {
               steps {
                      git 'https://github.com/SupleOm/HOD1.git'
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
			else if ( env.ENVIRONMENT == 'UAT' ){
    		sh 'cp target/HOD1.war /home/omsuple/Devopstool/apache-tomcat-9.0.93/webapps'
    		echo "deployment has been done on UAT!"
			}
			}}}	
}}
                              
