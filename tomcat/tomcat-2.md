## Apache Tomcat Folder Structure

- **conf** - Stores Tomcat's configuration files.
- **logs** - Stores the log files related to Tomcat operations.
- **webapps** - The default deployment directory for web applications.
- **work** - Stores compiled JSP files and servlet-generated code.
- **bin** - Contains scripts and executable files to start and stop Tomcat.
- **temp** - Used by Tomcat to store temporary files such as extracted `.war` files.

## How to Access the Application URL

```
127.0.0.1:8080 or localhost:8080
<url_of_tomcat>/<ArtifactName>
```

Example:
```
localhost:8080/aja
```
Where `aja` is the artifact name.

## Maven Command to Generate a Web Application Archetype

```sh
mvn archetype:generate -DgroupId=com.example.aja -DartifactId=aja -DarchetypeArtifactId=maven-archetype-webapp -DinteractiveMode=false
```

## How to Place the Artifact from the Maven Project's Target Folder to Apache Tomcat's Webapp Folder

```sh
cp <path_where_artifact> <path_where_webapps_of_tomcat>
cp <source> <destination>
<destination> cp /<source> .
```
*Note: While copying, use a forward slash (`/`).*

## Restarting the Server After Configuration Changes

If any configuration changes are made, restart the Tomcat server.

### To Stop Tomcat:
```sh
ctrl + c
```

## Changing the Port Number of Tomcat

To change the port number, stop and restart the server.

## Deploying the Application Using Apache Tomcat GUI

1. Access the Tomcat URL.
2. Search for the `.war` file to deploy.
3. Click on `Choose File` to open a dialog box.
4. Select the artifact and click `Open`.
5. Click on the `Deploy` button.

## How to Access Apache Tomcat GUI

1. Navigate to the Tomcat home folder.
2. The home folder of Apache Tomcat is located at `conf/`.
3. Modify `tomcat-user.xml` using a text editor (e.g., `vi`):
   ```sh
   vi tomcat-user.xml
   ```
4. Search for the line `<user username="admin"`.
5. Uncomment the necessary lines (`<!--` and `-->`).
6. Save and exit.

## Difference Between `pom.xml` and `settings.xml`

- Use `pom.xml` to define dependencies, plugins, and configurations specific to a project.
- Use `settings.xml` to configure Maven behavior globally, such as repository authentication and proxy settings.

## Viewing Specific Lines in a File

To view the last `n` number of lines:
```sh
tail -n filename
```

To view the first `n` number of lines:
```sh
head -n filename
```

