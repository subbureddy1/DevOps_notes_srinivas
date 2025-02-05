## configuration:
Things to keep in mind before changing configurational changes.
### where to change
### how to change
### Try or Experiment in local environments
### documentation


## snapshot/Backup:

For wildfly-configuration snapshot
-->Homefolder of wildfly-->standalone-->configuration-->standalone_xml_history
File name:standalone.v1
ex:port number change
standalone_portchange.v2
Need to rename the original or existed file and then replace the customised as per requirement/change

## different status of the artifacts deployed in wildfly:
In wildfly, deployed artifacts can have various status states including:

## deployed:
The application is successfully running on the wildfly server and accessible to users

## undeployed:
The application has been removed from the server and is not currently running.

## failed:
the deployment process encountered an error and the application is not running

## disabled:
the application is intentionally stopped by the administrator and cannot be accessed until enabled.

## suspended: 
the application is temporarily paused and can be resumed later

## redeploying: 
the application is currently being updated with new code and is not fully available while the redeployment process is ongoing

## Accessing deployment status:

### wild fly management console:

you can view the status of deployed artifacts through the wildfly admin console which provides a list of deployments with their current state.

### CLI(command Line Interface):
using the wildfly command-line interface you can query the status of deployments with management commands

indicating whether the application is currently running not deployed encountered an error during deployment,intentionally de activated temporarily paused or is in the process
of being redeployed with updates

## Domain & Host controller in wildfly:
In Jboss wildfly a "domain controller" is the central management point for a group of servers with in a domain responsible for maintaining the overall configuration and policy.

while a "host controller" is a separate process running on each server within the domain, communicating with the domain controller to manage the individual server instances on that host machine
essentially, the domain controller dictates the over all configuration and the host controllers execute those configurations on their respective servers.

## keypoints about domain and host controllers:

### Domain controller:
a)acts as the central management point for the entire domain
b)stores the domain wide configuration in a file called "domain.xml"
home folder-->domain-->configuration-->domain.xml
c)Responsible for distributing configuaration changes to all host controllers with in the domain.

### Host controller:
a) manages the application server instances running on a specifichost
b)reads its configuration from a "host.xml" file specific to that host
Home folder-->domain-->configuration-->host.xml
c)communicates with the domain controller to receive configuration updates and start/stop server instances.

DC HC-Domain Control Host Control
Domain is referring to centralised or master wildfly where we can manage other-(host) wildfly servers.