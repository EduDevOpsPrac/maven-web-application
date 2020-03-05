node{
  stage('SCM Checkout'){
    git credentialsid: 'bhabanidevops', url:'https://github.com/EduDevOpsPrac/maven-web-application.git'
  }
  
  stage('Compile-Package'){
    def mvn_home = tool name: 'maven3', type: 'maven'
    sh "${mvn_home}/bin/mvn clean package"
  }
  
  stage('Email Notification'){
    mail bcc: 'b.mohanty1985@gmail.com', body: '''Thanks, 
    Bhabani ''', cc: 'b.mohanty1985@gmail.com', from: '', replyTo: '', subject: 'Build Status', to: 'b.mohanty1985@gmail.com'
  }
}  
