### I Need to trigger on feb 8th saturday every minute and in every hour :
 
**Minute Hour DayofMonth Month DOW**
   
    * * 8 2 6
 
### Job configuration of build periodically trigger and poll SCM trigger :
 
* create new item --> triggers --> select check box build periodically or poll SCM --> once clicked on check box, scheduling comment box will be open up.
* There we need to give schedule as per requirement eg (* * 8 2 6) --> Save (check for the jobs whether running as per the schedule or not)
 
### Build after projects are built :
 
* Create more than 1 jobs in triggers option select build after other projects are built.
* After selecting the option, need to give projects to watch name and then click on save and check.
 
  **Eg:** job1,job2,job3
 
* For job2 , put the upstream project as job1
* For job3 , put the upstream project as job2
* When we build the job1 , once job1 completed automatically downstream project has to be build.
 
* **For job2, once you select built after other projects are built, and then select sub option trigger even if the build falls and then save.**
* For job1, do one mistake wantedly and check for the all the jobs.
 
## Pipeline Project :
  We are going for pipeline projects in order to secure the CI-CD pipeline code by storing in any of the repositories (github,gitlab,bigbucket)
 
* Sample hello-world script creation :
   
   * Click on new item , select pipeline and click on ok.
   * Go for pipeline in configuration, where we can define pipeline script.
   * We can script in script tag or else we can take it from SCM.
   * In the script tag, click on drop-down option to try sample pipeline.
 
 ```
pipeline{
    agent any
        stages{
            stage('hello'){
                steps{
                echo 'hello world'
            }
        }
    }
}
```
 
  * Click on save.
  * Make sure that stage view plugin should be installed, so that we can see stages.
 
### Rebuild VS Replay :
 
* When we use Rebuild , we are not changing anything, whereas Reply gives us prorision to change the code then and there.
* Replay , we also use it as one of the trouble-shooting mechanism.
 
* **If we do not know how to write pipeline script code, we can take the advantage of snippet generator in pipeline syntax option (pipeline syntax option will only visible when you create pipeline job or project.)**
* The **Snippet generator** will help you learn the pipeline script code which can be used to define various steps.
* Pick a step you are interested in from the list, configure it, click generate pipeline script, and you will see a pipeline script statement that would call the step with that configuration.
* You may copy and paste the whole statement into your script , or pick up just the options you care about.
 
**Eg :** To print message
 
* In sample step of snippet generator , search for the echo, there is a step **echo:print message** then what message we need to print we have to pass it in message block then click on generate pipeline script, which will give us script to print message
* By default pipeline execution will work on serially (one by one), if the previous stage is passed then only it will go for next or further stages.
 
### What is an API?
An API (Application Programming Interface) is a set of rules and protocols that allows different software applications to communicate with each other

### Purpose of an API
Enable Communication Between Systems

Automate Processes

Improve Scalability

Enhance Security

Standardize Data Exchange

### What is TDD (Test-Driven Development)?

TDD is a development approach where tests are written before the actual implementation of the code. The goal is to ensure that the code meets the specified requirements and functions correctly.

### What is BDD (Behavior-Driven Development)?

BDD is an extension of TDD that focuses on defining application behavior in a human-readable format. It encourages collaboration between developers, testers, and non-technical stakeholders (e.g., business analysts).