node{
   def tomcatWeb = 'C:\\apache-tomcat-10.0.0-M5-windows-x64\\apache-tomcat-10.0.0-M5\\webapps'
   def tomcatBin = 'C:\\apache-tomcat-10.0.0-M5-windows-x64\\apache-tomcat-10.0.0-M5\\bin'
   def tomcatStatus = ''
   
  stage('SCM Checkout'){
     git 'https://github.com/Hemantakumarpati/addressbook.git'
   }
  
   stage('Compile-Package-create-war-file'){
         bat "mvn package"
      }
   stage('Deploy to Tomcat'){
     bat "copy target\\addressbook.war \"${tomcatWeb}"
   }
      stage ('Start Tomcat Server') {
         sleep(time:5,unit:"SECONDS") 
         //bat "${tomcatBin}\\startup.bat"
         bat "C:\\apache-tomcat-10.0.0-M5-windows-x64\\apache-tomcat-10.0.0-M5\\bin\\startup.bat"
         sleep(time:100,unit:"SECONDS")
   }
}
