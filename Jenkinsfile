node{
   def tomcatWeb = 'C:\\apache-tomcat-8.5.58-windows-x64\\apache-tomcat-8.5.58\\webapps'
   def tomcatBin = 'C:\\apache-tomcat-8.5.58-windows-x64\\apache-tomcat-8.5.58\\bin'
   def tomcatStatus = ''
   
  stage('SCM Checkout'){
     git 'https://github.com/Hemantakumarpati/addressbook.git'
   }
  
   stage('Compile-Package-create-war-file'){
         bat "mvn package"
      }
   stage('Deploy to Tomcat'){
     bat "copy target\\*.war \"${tomcatWeb}"
   }
 
}
