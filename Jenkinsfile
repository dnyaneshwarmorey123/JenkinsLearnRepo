node{
     stage('SCM Checkout'){
     git 'https://github.com/dnyaneshwarmorey123/JenkinsLearnRepo'
     }
   
       
     
     
     stage('Compile-Package'){
     bat 'mvn clean install -DskipTests=true'
     }
     
     
     stage('Junit test cases'){
     bat "./mvnw test"
     }
    
     
     stage('Deploying artifacts'){
     deploy adapters: [tomcat8(credentialsId: 'c1366040-9762-4579-80ad-cd6831759dc0', path: '', url: 'http://localhost:8081/RestService-0.0.1-SNAPSHOT/Users/1')], contextPath: 'restServices', war: '**/*.war'
     }
}
