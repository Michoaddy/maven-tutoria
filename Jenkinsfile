 Feature-1

#Edited on Feature branch
node('master') 
 Loans
{
    stage('ContinuousDownload-Loans') 
    {
       git 'https://github.com/selenium-saikrishna/maven.git'

    }
    stage('ContinuousBuild-Loans') 
    {
      sh 'mvn package'
    }
    stage('ContinuousDeployment-Loans')
    {
        sh 'scp /home/vagrant/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war vagrant@10.1.1.5:/var/lib/tomcat7/webapps/loansenv.war'
    }
    stage('Continuoustesting-Loans')
    {
        git 'https://github.com/selenium-saikrishna/FunctionalTesting.git'
    }
    
    
 
    
    
    


node('built-in') 
 master
{
    stage('Continuous Download') 
	{
    git 'https://github.com/sunildevops77/maven.git'
	}
    stage('Continuous Build') 
	{
    sh label: '', script: 'mvn package'
	}
    stage('Continuous Deployment') 
	{
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war   ubuntu@172.31.26.217:/var/lib/tomcat8/webapps/qaenv.war'
	}
    stage('Continuous Testing') 
	{
              sh label: '', script: 'echo "Testing Passed"'
	}
    stage('Continuous Delivery') 
	{
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war   ubuntu@172.31.22.88:/var/lib/tomcat8/webapps/prodenv.war'
	}
master
}
