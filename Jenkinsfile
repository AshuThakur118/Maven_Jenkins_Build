pipeline {
   agent any 
   tools {
        maven 'maven-3.6.3' 
    }
   
   stages {
       stage('SCM CheckOut'){
          steps {
            git 'https://github.com/AshuThakur118/Maven_Jenkins_Build'
          }
          }
      stage('Compile-Package'){
         steps {
             sh "mvn -version"
             sh "mvn clean install" 
             sh "mvn package"
              }
         }
   }
   post {
      always {
         cleanWs()
      }
   }
}

