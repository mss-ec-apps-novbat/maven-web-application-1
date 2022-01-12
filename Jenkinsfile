node
{
  def MavenHome = tool name: "Maven3.8.4"  
	stage('CheckoutCode')
	{
		git branch: 'development', credentialsId: 'c67bf5a9-d717-4d60-8609-8c51e1be4d72', url: 'https://github.com/mss-ec-apps-novbat/maven-web-application-1.git'
	}	
    stage('Build'){
        sh "${MavenHome}/bin/mvn clean package"
    }
    /*
    stage('ExcuiteSonarQubeReport'){
        sh "${MavenHome}/bin/mvn clean sonar:sonar"
    }
   
   stage('UploadArtifactIntoNexus'){
       sh "${MavenHome}/bin/mvn clean deploy"
     
   } 
   
   stage('DeployAppintoTomcat'){
     sshagent(['ec69b0c4-549d-4b43-952a-5f199b8ed616']) {
    sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@13.233.247.166:/opt/apache-tomcat-9.0.56/webapps"
   }  
   
   }
 
   stage('SendNotifications'){
   emailext body: '''Build Over..

Regards,
Nagaraju''', subject: 'Build Over..', to: 'naga54710@gmail.com'    
   }    
 */ 
    
}
