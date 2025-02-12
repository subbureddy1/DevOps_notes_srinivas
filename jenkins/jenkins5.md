HOW TO CREATE A NEW ITEM PROJECT?

 * click on new item given the job name and select the item scroll down to bottom there you can see copy from option in that copy from tab we need to pass    the job name which we want to need to pass the existing job name which we want to make use of existing job configuration

EXAMPLE:~ create a job 10 .(take the reference of job8 configuration)


 HOW TO CHNAGE THE DEFAULT PORT NUMBERS OF JENKINS?

 * go to the path c:\programfiles\jenkins
 * in that folder find the jankins.xml file 
 * search for "--httpport=8080"in jenkins.xml file where 8080 is the default port number in order to change this default port number
   we should replace 8080 by our own port number then save it once modified this jenkins.xml file restart the jenkins server

 NOTE:~ before changing any jenkins configuration (or) port number better to take backup oforiginal file for safer side


 WHAT IF JENKINS ADMINISTRATOR FORGET FORGET PASSWORD?  
 
 * go to jenkins home directory C:\programData\jenkins\.jenkins in that path open config.xml file search for <use secirity> true</use security> replace true    with false <use security>false<\usesecurity> then save it then browser access the jenkins url where you will not see any login details & user detail in    jenkin GUI

 * go for the manage jenkins "security" undersecurity realm (where we change config.xml file from true to false it will be none) then we need to change    "none" to "jenkins" own user database 

 * authorization (when we chnage config.xml file from true to false authorization will change to any one can do any thing) here we need to change from any    one can do any thing to either martix based or project based strategy

 * once you select martix based or project based strategy under that uncheck the anonymous and click on add user button and add the admin user and give the    role  as administrator

 * then we have to save it;    manage jenkins -->user -->adminuser



 -> change the password then we have to save it.
 
 -> Now we need to restart the Jenkin Server.
 
 -> Notes Better take backup of config.xml file for Safe Side.
 
 -> Before restarting Jenkins
 
 -> once restarted check with admin user whether admin user has all the privileges or not.
 
 -> then go back to config.xml file and modify user security tag from false to true then restart the Jenkin server.
 
 Jenkins.io/doc/book/pipeline/jenkinsfile/#using-environment-variables

 Using Jenkins Environment Variables
 
 Jenkins pipeline Exposes Environment variables via the global variable Env, which is available from anywhere within a Jenkins file.
 
 -> Below are some environment variables.
 
 BUILD_ID - The current build ID, identical to BUILD_NUMBER for builds created.
 
 Likewise we have "BUILD_NUMBER", "BUILD_TAG", "BUILD_URL", "JENKINS_URL", "JOB_NAME", "NODE_NAME", "WORKSPACE"
 
 Here's how you can create your Word document:


 
 Jenkins pipeline Exposes Environment variables via the global variable Env, which is available from anywhere within a Jenkins file.
 
 -> Below are some environment variables.
 
 BUILD_ID - The current build ID, identical to BUILD_NUMBER for builds created.
 
 Likewise we have "BUILD_NUMBER", "BUILD_TAG", "BUILD_URL", "JENKINS_URL", "JOB_NAME", "NODE_NAME", "WORKSPACE





 Ex: Use the Jenkins file (Declarative pipeline) - https://jenkins.io/doc/book/pipeline/jenkinsfile/#using-environment-variables
 
 copy this code and create item in Jenkins for pipeline job replace the script with copied code and save it and run (or) build it Expected output should be   "Running 1 on http://localhost:8080/"
 
 Task - Even though we can change the default port number of Jenkins from 8080 to other port but here still showing default port number only figure it out.
 
 How to Parameterized the Jenkins Job?
 
 -> Parameters allow you to prompt users for one or more inputs that will passed into a build.
 
 -> Create New Job in General configuration of that job you can see the option "This project is parameterized" need to check box that and there you will         option add parameter dropdown. Click on that you will see various parameters those are Boolean choice, Credentials, file, multi-line string, password,       Run, string.
 

 -> For example, click on choice parameter (defines a simple string parameter, which can be selected from a list you can use it during a build) give the     name as Env, and choices you can give more than one environment name and under description that will be shown to the user and click on Save.
 
 -> When you check the job to be triggered you will see build with Parameters option click on that and select the choices which we configured and go for the     build button.
 
 -> Another way of Creating Jenkins user?
 
    Manage Jenkins -> security -> directon the disable "keep"
