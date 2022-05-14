node('built-in') 
{
    stage('Continuous Download_loans') 
	{
    git 'https://github.com/sunildevops77/maven.git'
	}
    stage('Continuous Build_loans') 
	{
    sh label: '', script: 'mvn package'
	}
    stage('Continuious deploye') 
      {
    sh 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war ubuntu@172.31.9.244:/var/lib/tomcat8/webapps/qaenv.war'
     }
stage('Continuious Test') 
      {
    sh 'echo "test passed"'
     }
stage('Continuious Delivery') 
      {
    sh 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war ubuntu@172.31.10.51:/var/lib/tomcat8/webapps/prodenv.war'
     }
}

}
