node{
     stage('SCM Checkout'){
     git 'https://github.com/dnyaneshwarmorey123/JenkinsLearnRepo'
     }
   
     stage('Perl script'){
     bat "perl script.pl"
     }    
     
     
      stage('Compile-Package'){
     bat 'mvn clean install -DskipTests=true'
     }
     
     
   
    
     
     stage('Deploying artifacts'){
     deploy adapters: [tomcat8(credentialsId: 'c1366040-9762-4579-80ad-cd6831759dc0', path: '', url: 'http://localhost:8081/manager/html')], contextPath: 'restServices', war: '**/*.war'
    
     }
}
