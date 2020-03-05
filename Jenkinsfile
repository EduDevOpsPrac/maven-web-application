node{
  stage('SCM Checkout'){
    git credentialsid: 'bhabanidevops' url:'https://github.com/EduDevOpsPrac/maven-web-application.git'
  }
  
  stage('Compile-Package'){
    sh 'mvn clean package'
  }
}  
