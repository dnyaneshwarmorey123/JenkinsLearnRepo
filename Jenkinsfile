node{
     stage('SCM Checkout'){
     git 'https://github.com/dnyaneshwarmorey123/JenkinsLearnRepo'
     }
   
       
     
     
      stage('Compile-Package'){
     bat 'mvn clean install -DskipTests=true'
     }
     
     
   
    
     
     stage('Deploying artifacts'){
     deploy adapters: [tomcat8(credentialsId: '0ed4a495-65a9-48af-b297-857ba7ad0888', path: '', url: 'http://localhost:8081/manager/html')], contextPath: 'restServices', war: '**/*.war'
     }
}
