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
     deploy adapters: [tomcat8(credentialsId: '2d4d4844-01dc-437e-b8f9-0c0b59f7d8a6', path: '', url: 'http://localhost:8081/manager/html')], contextPath: 'RestService-0.0.1-SNAPSHOT', war: '**/*.war'
     }
}
