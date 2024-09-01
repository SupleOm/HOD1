pipeline {
       agent{
           label 'slave-label'
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
              sh 'cp target/HOD1.war /home/omsuple/Devopstool/apache-tomcat-9.0.93/webapps'                
}}}	
}
                              
