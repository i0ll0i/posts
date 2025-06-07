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

In the Welcome screen click Next to continue.

![](images/welcome-screen.png)

The next step is the `Auto Updates` screen. Leave the default value for now that allows you to skip auto updates and click `Next`.

![](images/auto-update-screen.png)

In the next screen, you’ll be asked to specify the `Oracle Home` directory where WebLogic and other Oracle software will be installed. Either select an existing directory or create a new one.

![](images/installation-location.png)

The next screen will prompt you to select the installation type. Choose `WebLogic Server` if you need a minimal installation without extra components. For large-scale, clustered environments with high-performance requirements, you should choose Coherence. Choose `Complete with Examples` if you’re exploring WebLogic, learning how to use it, or testing applications based on the provided examples.

![](images/installation-type.png)

Then the installer will perform a series of prerequisite checks to ensure your system meets the requirements. If everything passes, click `Next`. If any issues are detected, you will need to resolve them before proceeding.

![](images/prerequisite-checks.png)

The next screen displays a summary of the installation, including the components to be installed and the selected directories.

![](images/installation-summary.png)

In the next step, the installer will begin copying files and configuring WebLogic Server. This process can take several minutes.

![](images/installation-progress.png)

Once the installation finishes, leave the `Automatically Launch the Configuration Wizard` option active and click `Finish`.

![](images/installation-complete.png)

## Сreating a domain

After installing WebLogic, you need to create a domain to run your WebLogic instances. To do this, select Create a new domain, specify the domain location, and click `Next`.

![](images/configuration-type.png)

Then, select `Create Domain Using Product Templates` and choose `Basic WebLogic Server Domain` for a simple domain setup. If you require advanced features, select them as needed.

![](images/templates.png)

Provide a username and password for the WebLogic Admin account. The default username is `weblogic`.

![](images/admin-account.png)

Choose either `Development` for development purposes or `Production` for a production environment. Ensure that the JDK points to the correct version.

![](images/domain-mode-and-jdk.png)

In the next screen, select `Administration Server`. Choose `Node Manager` if you plan to manage multiple Managed Servers or set up clusters. The Topology option is necessary if you’re going beyond a simple single-server setup.

![](images/advanced-configuration.png)

Specify the admin server’s settings, such as the server name and port. The default admin server runs on port `7001`.

![](images/administration-server.png)

Then, select `Create` to accept the above options and start creating and configuring a new domain.

![](images/configuration-summary.png)

Click `Next` after completing the creation and configuration of a new domain.

![](images/configuration-progress.png)

In the final window, select `Start Admin Server` and click `Finish`.

![](images/end-of-configuration.png)

After the server starts successfully, open a web browser on your server and go to `http://localhost:7001/console`. Log in using the credentials you created earlier.

![](images/welcome-page.png)

After successful login, you’ll be redirected to the Administration Console dashboard.

![](images/dashboard.png)

## Conclusion

So we looked at how to install Oracle WebLogic on Windows Server 2019. Logging into the WebLogic Admin Console provides comprehensive control over your WebLogic environment, making it the primary tool for administrators to manage the entire server domain.
