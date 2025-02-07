## What if jenkins user forget the password ?
  * As the jenkins administrator there is a prevision to reset the user's credentails.
 
  manage jenkins --> security --> user's --> go for the user which need to be reset and click on security (left side you will see the option)
 
  * see password and confirm password. There you can change the password and click on save .
  * Once as a administrator change the password again you need to inform to the user saying please , follow the below steps to login.
  * Once loged into the jenkins GUI , click on user name
  * Click on security -> their you can change the password.
 
**Note :**  Slaves, nodes , agents these three terminologies are same.

### what if Jenkins administrator forget the password?(task)

If a Jenkins administrator forgets the password, they can reset it using one of the following methods:

--> Delete the Admin Password from config.xml

--> Reset Admin Password via User XML File

## Jenkins Folders :
   In windows o.s we can see all jenkins information and configuration under path
       
    C:\ProgramData\Jenkins\.jenkins\workspace\demo>dir
 
* Under .jenkins folder we can see
   
   * **Users :** where all the jenkins user data is available.
   * **Workspace:** where all the configured jobs information available.
   * **Secrets:** Where all the configured secrets are available
   * **Plugins:** all the plugins (which are in installed manually and automating)available.
   * **Nodes:** where all the configured nodes are available
   * **Logs:** we can see slaves (if configured) and tasks logs are available.
   * Apart from the above folders there is jenkins configurational file namely **config.xml** (if at all changing config.xml file first take the backup of the file )

   * We can also see the jenkins logs in GUI
   
   manage jenkins --> status information --> system log --> all jenkin logs
 
## Where we can see the jenkins version?
  We can see the jenkins version at the bottom of jenkins GUI and also
     
manage jenkins --> status information --> about jenkins
 
Ways to trigger the jenkins jobs :
 
**Triggers:** Setup automated actions that start your build based on specific events , like code changes or scheduled times.
 
* 5 ways :
   
   * **Trigger builds remotely (eg , from scripts) :** In order to use this option / trigger , first we need to generate the authentication token of the job.
   * Enable this option if you would like to trigger new builds by accessing a special pre-defined URL (Convenient for scripts)
   * You need to provide an authorization token in the form of string so that only those who know it would be able to remotely trigger this project's builds.
   * This is most useful when your jenkins instance grants read access to this job to anonymous users.
   * When that's not the case, jenkins will reject requests sent to the trigger URL even when the correct token is specified
   * Use the following URL to trigger build remotely :
 
    JENKINS_URL/job/ajafreestyle/build?token=TOKEN_NAME or /buildWithParameters?token=TOKEN_NAME
 
**2 . Build after other projects are built (upstream and downstream jobs):**
 
* setup a trigger so that when some other projects finish building, a new build is scheduled for this project.
* This is convenient for running on extensive test after a build is complete.
* We need to pass the job name (which are configured already  under projects to watch tab )
 
 * Under projects to watch , there are 4 options
 
 1. Trigger only if build is stable
 2. Trigger even if the build is unstable
 3. Trigger even if the build fails
 4. Always trigger , even if the build is aborted.
 
**3. Build periodically(in schedule):**
 
* This field follows the syntax of **CRON** (with minor differnces). Specifically, each line consists of 5 fields separated by TAB or whitespace.
 
   **MINUTE HOUR DOM MONTH DOW**
 
**Minute :** Minutes within the hour (0-59)
 
**Hour:** The Hour of the day (0-23)
 
**DOM:** The day of the month (1-31)
 
**Month:** The Month (1-12)
 
**DOW:** The day of the week (0-7) where 0 and 7 are sunday.
 
* To specify multiple values for one field, the following operation are available.
* For reference / Practice use this website
 
      crontab.guru
 
**4.Github hook trigger for GIT SCM Polling :**
 
  When jenkins receives a github push hook , Github plugin checks to see whether the hook came from a github repository  which matches the Git repository defined in SCM/Git section of this job.
 
**5.Poll SCM :** Configure jenkins to poll changes in SCM.

### Why Use Git Webhooks in Jenkins?

Git webhooks in Jenkins automate the process of triggering builds whenever there is a code change in a repository.
 
### Purpose of Git Webhooks in Jenkins
Automated Build Trigger

When a developer pushes code to Git, Jenkins receives an event via a webhook and triggers a build automatically.

### Reduced Load on Jenkins Server

Polling Git repositories at intervals (e.g., every minute) can cause unnecessary load.
Webhooks notify Jenkins instantly, reducing server resource usage.

### Faster CI/CD Pipeline Execution

Immediate triggering of builds speeds up feedback loops.

Developers can quickly identify and fix issues.

### Efficient Deployment Pipeline

Webhooks ensure code changes are tested and deployed faster.

They help integrate Jenkins with DevOps workflows, making deployments more seamless.

### Better Integration with SCM Tools

Jenkins can be integrated with GitHub, GitLab, Bitbucket, etc., using webhooks.
Supports push events, PR events, tag creation, branch deletions, etc.

### How to Configure Git Webhooks in Jenkins?
Enable "GitHub hook trigger for GITScm polling" in the Jenkins job.
Set up a webhook in GitHub/GitLab:

Go to the repository → Settings → Webhooks → Add Webhook.
Provide the Jenkins webhook URL:

http://<JENKINS_URL>/github-webhook/

Select "Just the push event" or other events as needed.

Ensure Jenkins is accessible from GitHub (configure a public IP or set up a reverse proxy).

Test the webhook by pushing code and checking if Jenkins triggers the build.

**Note:** We can also trigger the job in manually
 