pipeline {
   agent any

   stages {
   
    stage('checkout') {
         steps {
          /* http://10.61.43.73:8081/ in/javahome/Publish.zip/1/Publish.zip-1.zip */   
             http://10.61.43.73:8081/repository/simpleapp-release/in/javahome/Publish.zip/1/Publish.zip-1.zip
         }
      }
   
      stage('Deploy') {
         steps {   
        bat label: '', script: ' C:/"Program Files (x86)"/IIS/"Microsoft Web Deploy V3"/msdeploy.exe -verb:sync -source:package="Publish.zip" -dest:auto -setParam:name="IIS Web Application Name",value="Default Web Site/Publish"'
         }
      }
      
   }
}
