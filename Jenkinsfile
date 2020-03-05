node{
  stage('SCM Checkout'){
    git credentialsid: 'bhabanidevops', url:'https://github.com/EduDevOpsPrac/maven-web-application.git'
  }
  
  stage('Compile-Package'){
    def mvn_home = tool name: 'maven3', type: 'maven'
    sh "${mvn_home}/bin/mvn clean package"
  }
  
  sshagent(['tomcatID']) {
    sh 'scp -o StrictHostKeyChecking=no target/*war ec2-user@172.31.2.193:/opt/apache-tomcat-9.0.31/webapps/'
  }   
 
}  
        
    
  
