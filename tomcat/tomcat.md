# Apache Tomcat

Apache Tomcat is an open-source web server and servlet container for Java code.

---

## How to Install Apache Tomcat on Windows

### Prerequisites:
- Java JRE installed and configured
- Administrative privileges

### Step 1: Download Tomcat for Windows
- Browse to the official [Apache Tomcat Website](https://tomcat.apache.org/) and download the appropriate version.

### Step 2: Install Tomcat
- Use the Windows Service Installer for an automated, wizard-guided installation.
- Alternatively, download the **32-bit/64-bit Windows ZIP file** based on your Windows version.
- Extract the ZIP file:
  - Right-click the file and select **"Extract All"**.
  - Navigate to the extracted Apache Tomcat folder.

### Default Port Number
- Apache Tomcat runs on **port 8080** by default.
- To change the port number:
  - Navigate to:  
    ```
    ApacheTomcat → conf → server.xml
    ```
  - Open `server.xml` and locate the following section:

    ```xml
    <Connector port="8080" protocol="HTTP/1.1"
        connectionTimeout="20000"
        redirectPort="8443" />
    ```

  - Change the `port="8080"` to any number between **1024 and 65535**.

---

## How to Start and Stop Apache Tomcat

### Start Tomcat:
Navigate to:
ApacheTomcat → bin → startup (Windows Batch File)


### Stop/Shut Down Tomcat:
Navigate to:
ApacheTomcat → bin → shutdown (Windows Batch File)

---

## Configuration and Deployment

### Configuration Changes:
ApacheTomcat → conf

### Hosting Applications (Artifacts/Deployable Packages):
ApacheTomcat → webapps

### Logs:
ApacheTomcat → logs

Logs include:
- **Apache Tomcat logs**
- **Application logs** (for applications running inside Tomcat)

### Access Apache Tomcat:
- Open a web browser and go to:

http://localhost:8080

http://127.0.0.1:8080
