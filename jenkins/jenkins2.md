## Plugin installation

there are two ways to install the plugins

1) automatic
2) manual

### Automatic

once we login to jenkins GUI, left side you will see the option "manage jenkins"

click on manage jenkins, in first tab there is system configuration under that we can see plugins

click on plugins go to available plugins and search for the plugin which is required

select the plugin under the list once you select the plugin install button will be highlighted, then click on install button.

### manual

Under plug-ins tab, go for available plug-ins and search for the plug-in, click on the plug-in which is required.
 
Once you click on the plug-in new tab will be opened, then click on releases and under releases you can see various versions of the plug-ins.
 
Go for the plug-ins which is required specific version.
 
Click on 'direct link' in installation options, once you click on Direct link plug-in will get downloaded to our local machine.
 
When we download plug-in in manual way again we need to deploy it to Jenkins.
 
In Jenkins GUI plug-ins tab, Click on advanced settings.
 
Choose the file to upload which is downloaded to local machine.

## plugins

add,remove,disable or enable plugins that can extend the functionality of jenkins

when we install plugins through automatic way, plugins extension is .JPI(jenkins plugin)

when we install plugins through manual way, plugins extension is .HPI(hudson plugin)

### how to uninstall the plugin

manage jenkins ---> plugin ---> installed plugins---> search plugin and then uninstall button will be highlighted.

once clicked on uninstall, plugin will getnunistalled.

### how to update the plugin:

manage jenkins ---> plugin --->updates

Select the plugin and then update button will be highlated, once clicked on update , plugin will get updated.

In real time , we should not update the plugin directly, reason being they may be a challanges encounted

It will be recommended to update the plugin in our local system where other team members will not affected if anything goes wrong.

## How to create the users ?
  manage jenkins --> security --> users

### Users : ( Create / delete / modify users that can log into this jenkins)
 
Click on users, you will be seeing craete user option.

Click on create user , fill all the details and then click on create user .

## How to give permission to the users ?

manage jenkins --> Security ( Secure jenkins define who is arrowed to access / use the system)
 
Click on that security , you will go to authorization page.

Under that you will be seeing add user button

Click on that add user button

It will ask user ID and give userID and click ok button

After that you should see added user name

Then give the permissionfor the users by checking the box (Minimun Access to give is overall Read)

By default, what ever we create the users, will get stored in Jenkin's own user database.
 
Jenkin's own user database is suitable for smaller setup where you have no existing user datadata use where.

Other option is **LDAP** ( Light Weight Directory Access Protocol)

## Authorization Stratergies :

By default you can see project-based matrix authorization stratergy, with this we can manage the authorization based on the options available under stratergy.
   
Eg: Credentials, Agent, Job, Run, view etc ...

### Matrix  authorization stratergy :
It allows configuring the lowest level permisiion such as starting new build , configuring items or deleting them , individually.
 
## Jenkins projects ( Projects or jobs both are same )
It is a combination of one or more tasks.
 
Free style project:
Classic, general-purpose job type that checks out from up to one SCM, executes build steps serially, followed by post-build steps like archiving artifacts and sending email notifications.

pipeline:
Orchestrates long-running activities that can span multiple build agents. Suitable for building pipelines(formerly known as workflows) and /or organizing complex activities that do not easily fit in free-style job type

multi-configuration project:
Suitable for projects that need a large number of different configurations, such as testing on multiple environments, platform-specific builds, etc.

Folder:
Creates a container that stores nested items in it. Useful for grouping things together. Unlike view, which is just a filter, a folder creates a separate namespace, so you can have multiple things of the same name as long as they are in different folders

Multibranch pipeline:
creates a set of pipeline projects according to detected branches in one SCM repository.

Organization Folder:
Creates a set of multibranch project subfolders by scanning for repositories.

 
These are default things we will get after creating the project.
 
**RBAC :** ( Role Based Access control ) one of the way where we can secure the jenkins

## How to create the job or project :

In Jenkins GUI, you will see "+" new item on the left side
   
Click on that new item , enter an item name then select an item type , once selected any of the item.

Click ok button which will be highlated

Job configuration is consists of (Where we can give information / description about the project)

Source code management where will be passing url's of the repositories

Build triggers (In what way we wanted to trigger build that job), build environments , build step (where we can add tasks)

Post build action
 
## How to get free style job :

new item -> give job name /  item name -> select free style project -> ok
 
Build steps (configuration) -> add build step dropdown --> select execute windows batch command --> type dir --> click on save
 
then click on build now & check for console output.

blue ocean(plugin)rethinks the Jenkins user experience designed from the ground up for Jenkins pipeline and compatible with freestyle jobs.



