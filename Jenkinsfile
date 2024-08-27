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
                 script{
if [ env.ENVIRONMENT = "QA" ];then
	cp target/HOD1.war /home/omsuple/Devopstool/apache-tomcat-9.0.93/webapps
elif  [ env.ENVIRONMENT = "UAT" ];then
         cp target/HOD1.war /home/omsuple/Devopstool/apache-tomcat-9.0.93/webapps
echo "deployment has been done!"
fi

}
                  }
        }
}
}             
