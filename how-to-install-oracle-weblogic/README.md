# How to Install Oracle WebLogic

Oracle WebLogic is a Java EE application server used to develop, deploy, and manage enterprise-level applications. It supports a variety of Java-based applications and offers features like clustering, high availability, and load balancing for scalable and fault-tolerant environments. WebLogic integrates with Oracle’s Fusion Middleware stack and is commonly used in complex IT infrastructures. It also provides a web-based administration console for managing servers, applications, and system resources. With built-in support for JMS, JDBC, and JNDI, it’s ideal for handling distributed systems and large-scale application hosting.

Before installing WebLogic on Windows Server 2019, you must [install and pre-configure JDK 8](https://iolloi.icu/index.php/2024/09/23/how-to-install-jdk-8-on-windows-server/). WebLogic uses JDK 8 to provide the necessary runtime environment, language features, and libraries for executing Java EE applications, ensuring compatibility, security, and performance. JDK 8 is a version of the Java Development Kit that provides the tools, libraries, and runtime environment needed for developing and running Java applications.

## How to Install Oracle WebLogic

To download WebLogic, go to the [Oracle Technology Network](https://www.oracle.com/middleware/technologies/weblogic-server-downloads.html) and log in to the site. Select the appropriate version of WebLogic Server and download the installer.

![](images/download-page.png)

Once the download is complete, extract the contents of the archive to your JDK directory. For example, `C:\Program Files\Java\jdk1.8.0_202`. In our case, the archive contains `fmw_14.1.1.0.0_wls_lite_generic.jar` file.

Open a command prompt, navigate to the directory where the `*.jar` file is located, and run the installation using the command:

`java -jar fmw_14.1.1.0.0_wls_lite_generic.jar`

This will launch the WebLogic Server installer.

Continued on the [iolloi.icu](https://iolloi.icu/index.php/2024/10/10/how-to-install-oracle-weblogic/)
