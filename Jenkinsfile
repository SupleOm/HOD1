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
                 sh 'JAVA_HOME=/home/grras/slavedir/jdk-11.0.24 /home/grras/slavedir/apache-maven-3.9.8/bin/mvn install'
                     } }
            stage('deploy'){
               steps{
              sh 'cp target/HOD1.war /home/grras/slavedir/apache-tomcat-9.0.93/webapps'                
}}}	
}
                              
