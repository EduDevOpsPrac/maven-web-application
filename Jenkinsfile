node{
  stage('SCM Checkout'){
    git credentialsid: 'bhabanidevops', url:'https://github.com/EduDevOpsPrac/maven-web-application.git'
  }
  
  stage('Compile-Package'){
    def mvn_home = tool name: 'maven3', type: 'maven'
    sh "${mvn_home}/bin/mvn clean package"
  }
}  
