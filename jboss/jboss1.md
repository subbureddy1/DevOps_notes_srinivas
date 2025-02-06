### what is Jboss?
Jboss is a powerful open source java application server developed by Redhat.

website name:wildfly.org/downloads/
current version is 35

admin port no:9990

application port no or artifacts:8080

Admin: <URL:9990>
Application:<URL:8080>/<application-name>

### Folder structure of the Jboss wildfly

domain

modules

welcome-content

docs

bin

appclient

standalone (configuration & deployments)

one of the folder in folder structure standalone where we will be having the configuration and deployment folder and logs.

configuration:where we will be having configurations of applications, users specifics.

ex:mgmt-users.properties and mgmt-groups.properties

Logs:standalone -->log -->logs of the wildfly

### To start the Jboss go to the home folder of the wildfly then bin folder

Home folder of wildfly-->bin
Filename:standalone(windows batch file)

### How to shutdown Jboss wildfly in windows(task)?
bin-->jboss-cli.bat(click on this file and type command shutdown)

### How to create management console user?
management console user:
<Home folder of wildfly>-->bin
filename:add-user(windows batch file)

once you run that add-user file we will get this console
what type of user do you wish to add?
a)management user(mgt-user.properties)
b)application user(application-user.properties)



It will going to ask me the username after username it will ask you for the password after setting password it will ask you to reenter the password.

Admin/management console:<URL:9990>

username & password

## Deployments:
A deployment represents anything that can be deployed(ex: an application such as EJB-JAR,WAR,EAR any kind of standard archive such as RAR or JBOSS-specific deployments)in to a server
you can use drag and drop to add new content or replace existing deployments simply drag one or several files on to the deployment column.
If there is already a deployment with the same name the deployment will be replaced otherwise the deployment will be added.The deployments added by drag and drop will be enabled by default.
Left side when you click on plus symbol you will see options like upload deployment, unmanaged deployment,create empty deployment
clicking on upload deployment

### How to deploy the application or artifacts to the wildfly?
a.copying the war file and pasting it deployment folder of wildfly(Home of wildfly -->standalone -->deployments)
b.cp <artifact sourcepath> <destination of deployments of wildfly>
c.Jboss wildfly GUI-->upload Artifact

### How we can change default port numbers of wildfly (9990 and 8080)task.
standalone-->configurations-->standalone.xml and standalone-full.xml(change port numbers here)

### How we can configure master/slave architecture in wildfly
Domain Mode: WildFly must be run in domain mode to enable master/slave functionality. 
Domain Controller: The master server acts as the domain controller, responsible for distributing configuration and deployments to the slave servers. 
Configuration File: The domain.xml file defines the domain configuration, including the master and slave servers, and their communication details. 