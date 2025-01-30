# Maven through Terminal

## Install Maven Tar File and Verify Signature  

After installing Maven, check its version from the Ubuntu terminal using the command:  
mvn -version

Create a Maven Project
Use the following command to create a project using Maven:

mvn archetype:generate -DgroupId=com.example-DartifactId=helloworld-DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false

Maven Lifecycle Phases (8 Phases)
1. Validate
Checks if the project is correct, having all the necessary information.
mvn validate

2. Compile
Compiles the source code of the project.
mvn compile

3. Test
Tests the compiled source code using a suitable unit testing framework. These tests should not require the code to be packaged or deployed.
mvn test

4. Package
Takes the compiled code and packages it in its distributable format, such as JAR.
mvn package

5. Integration-Test
Processes and deploys the package into an environment where integration tests can be run.
mvn integration-test

6. Verify
Runs any checks to verify that the package is valid and meets quality criteria.
mvn verify

7. Install
Installs the package into the local repository for use as a dependency in other projects locally.
mvn install

8. Deploy
Copies the final package to the remote repository for sharing with other developers and projects.
mvn deploy

Note: When running any Maven lifecycle phase, all previous phases are executed as well.
Example: Running mvn package (4th phase) will also run validate, compile, and test.

What is the .m2 Folder?
The .m2 folder is the local repository of Apache Maven.

Path example:

Windows: C:\Users\username\.m2
Linux/Mac: ~/.m2
arduino

This Markdown-formatted text is ready for use in any `.md` file or Markdown-supported platform.