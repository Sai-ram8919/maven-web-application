node
{
    def mavenHome = tool name: "Maven3.9.9"
    
    stage('CheckoutCode')
    
    {
     git credentialsId: '48282386-2ee9-4bed-9197-33c2df6f4d3e', url: 'https://github.com/Sai-ram8919/maven-web-application.git'
    }
    
    stage('Build')
    {
        sh "${mavenHome}/bin/mvn clean package"
    }
    /*
    stage('UploadartifactIntoNExus')
    
    {
     sh "${mavenHome}/bin/mvn deploy"
     
     stage('DeployAppIntoTomcat')
     {
         sshagent(['d9931b2d-a18a-4403-b493-236db7262e40']) 
         {
sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ubuntu@15.206.185.131:/opt/apache-tomcat-9.0.97/webapps/"
         }
     }
    }
    
    stage('SendEmailNotification')
    {
        mail bcc: '', body: '''Buils Status 

Regards,
Sai Rampelli (DevOps Engineer)
8919715494''', cc: '', from: '', replyTo: '', subject: 'Build Status ', to: 'reachsai8919@gmail.com'
    }
   */ 
}
