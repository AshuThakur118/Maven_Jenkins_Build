pipeline {
   agent any 
   tools {
        maven 'Maven3.6.3' 
    }
   
   stages {
       stage('SCM CheckOut'){
          steps {
            git 'https://github.com/AshuThakur118/Maven_Jenkins_Build'
          }
          }
      stage('Compile-Package'){
         steps {
             bat "mvn -version"
             bat "mvn clean install" 
             bat "mvn package"
              }
         }
   }
   post {
      always {
         cleanWs()
      }
   }
}

