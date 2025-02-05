## CICD (CONTINUOUS INTEGRATION AND CONTINUOUS DELIVERY)

### CONTINUOUS INTEGRATION
### Improves quality
improves the quality by running multiple unit tests and analysis various static code

### Increases productivity
automating build of code saves a lot of time thereby increasing productivity

### Reduces risk 
eliminate the risk of potential human errors by automating test.

## Introduction to Jenkins
### features of jenkins
easy installation process

upgrades are easily available

provides advance security

lightweight container support

optimized performance 

distributed team management

### what is continuous integration
 process of automating the build and testing of code each time one of the team member commits changes to version control.

 CI: CONTINUOUS INTEGRATION
 CD: CONTINUOUS DELIVERY
   : CONTINUOUS DEPLOYMENT
delivery also knows release

CICD TOOLS:
Gitlab ci
code ship
bambo
jenkins
teamcity
travis ci

## from aws cloud:
if we wanted to perform cicd there are various services like code commit, code deploy, code build, code pipeline, code guru

## from azure cloud:
azure repos, boards, pipeline, test plans, artifacts

## what is jenkins
A continuous integration server which manages and control proceses such as plan, code, build, test, deploy, operate and monitors in devops environment.

## Why Jenkins is so popular?
- Open source
- Good plugin support
- Good community support
- Fast and reliable
- Good OS support
- Scripted builds

## Topics
Following are the topics covered in this module:

- **Jenkins Architecture**
- **Plugin Management in Jenkins**
- **Jenkins Security Management**
- **Notification in Jenkins**
- **Jenkins Master-Slave Architecture**
- **Jenkins Delivery Pipeline**
- **Jenkins Declarative Pipeline**

## Plugin Management in Jenkins
### Plugin: 
To have extra functionality

### Tabs:
- **Update**: Shows updates to plugins already installed
- **Available**: Shows plugins that are available for installation
- **Installed**: Displays plugins installed that have no updates
- **Advanced**: Lists configuration of HTTP proxy, allows manual upload of plugin and URL of plugin site

In real-time, we cannot install plugins as simple as that because there might be challenges with proxy settings as well as VPN (Virtual Private Network). To avoid this, we should configure HTTP proxy in Jenkins plugin of the advanced tab.

## How to Install Jenkins on Windows
### Different Ways of Installation:
- Using Docker
- Using Kubernetes
- Using Linux
- Using WAR file
- Offline Installations
- macOS

## Prerequisites
### Minimum Hardware Requirements:
- 256 MB of RAM
- 1GB of drive space (although 10GB is a recommended minimum if running Jenkins as a Docker container)

### Recommended Hardware Configuration for Small Team:
- 4GB+ of RAM
- 50GB+ of drive space

Jenkins tool is developed on Java code.

### Prerequisites:
- A system running Windows 10
- The latest copy of JDK OR JRE installed
- Access to an account with administrator privileges

[Jenkins LTS Download](https://jenkins.io/download/)

### Steps:
1. Browse to the downloads page of Jenkins under the downloading Jenkins section.
2. Click the Windows link to begin the download. Download Jenkins 2.479.3.
3. After downloading, go to the downloaded folder and double-click on Jenkins (Windows Install Package).
4. The setup wizard starts; click **Next** to proceed.
5. Select the install destination folder and click **Next** to continue.
6. Under the "Run Service as a Local or Domain User" option, enter the domain username and password for the user account you want to run Jenkins with.
   - Click "Test Credentials" to verify the login data, then click **Next** to proceed.
7. **Logon Type**:
   - First option: Run service as Local System (not recommended)
8. Enter the port number you want Jenkins to run on. Click "Test Port" to check if the selected port is available, then click **Next** to continue.
   - Default port number of Jenkins: **8080**
9. Select the directory where Java is installed on your system and click **Next** to proceed.
10. Select the features you want to install with Jenkins and click **Next** to continue.
11. Click **Install** to start the installation process.

## How to Configure Jenkins
### Steps:
1. After completing the installation process, you have to unblock Jenkins before you can customize and start using it.
2. In your web browser, navigate to the default port number you selected during the installation:
   ```
   http://localhost:8080
   ```
3. Navigate to the location on your system specified by the **Unblock Jenkins** page.
4. Copy the password from the following location:
   ```
   c:/ProgramData/Jenkins/.jenkins/secrets/initialAdminPassword
   ```
   - To read the data from the file, use the **cat** command:
     ```
     cat c:/ProgramData/Jenkins/.jenkins/secrets/initialAdminPassword
     ```
5. Copy the password from the **Initial Admin Password** file.
6. Paste the password in the **Administrator Password** field on the **Unblock Jenkins** page and click **Continue** to proceed.
7. Once you unlock Jenkins, customize and prepare the Jenkins environment.
8. Click the **Install Suggested Plugins** button to have Jenkins automatically install the most frequently used plugins.
9. After Jenkins finishes installing the plugins, enter the required information on the **Create First Admin User** page. Click **Save and Continue** to proceed.

## How to Stop the Jenkins Server on Windows:
1. In Windows **Search** option, search for **Services** and select Jenkins.
2. On the left side, click **Stop**.

##  How to Restart Jenkins:
### Safe Restart:
- Go to the URL of Jenkins:
  ```
  http://localhost:8080/safeRestart
  ```
- Jenkins will try to pause jobs and restart once all running jobs are either finished or paused.
- "Jenkins is Restarting" banner will be displayed on most Jenkins pages.
- You can use it to let users know what is happening. A default message will be added if you don’t supply one.
