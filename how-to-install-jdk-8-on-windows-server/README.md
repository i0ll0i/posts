# How to Install JDK 8 on Windows Server

The JDK (Java Development Kit) is a software development kit provided by Oracle and other vendors that is used for developing Java applications. It contains everything a programmer needs to write, compile, and run Java programs.

JDK 8 (also known as Java SE 8) is one of the most significant versions of the Java Development Kit, released by Oracle in March 2014. It introduced several important new features that significantly enhanced the Java language and its ecosystem. JDK 8 became a long-term support (LTS) release and remained one of the most widely adopted versions of Java for several years.

In this article, we will look at how to install and configure JDK 8 on Windows Server 2019.

## How to Install and Configure JDK 8

To install Java 1.8 (JDK 8) visit the [official Oracle Java SE page](https://www.oracle.com/java/technologies/javase/javase8-archive-downloads.html) and download the `.exe` file for 64-bit Windows systems.

![](images/download-page.png)

Once the download is complete, locate the `.exe` file and double-click it to launch the installer. The installer will guide you through the installation process. By default, the JDK will be installed in `C:\Program Files\Java\jdk1.8.x_xxx` directory.

After installation, you’ll need to set up the necessary environment variables (`JAVA_HOME` and update `PATH`). To do this, right-click on `This PC` and choose `Properties`. Then click `Advanced system settings`. In the `System Properties` window, go to the `Advanced` tab and click the `Environment Variables` button.

![](images/environment-variables.png)

Under `System Variables`, click `New` and add a new variable `JAVA_HOME` that contains the path to your JDK installation as the variable value.

![](images/JAVA_HOME.png)

Close the `New System Variable` window by `OK` button. Then select the `Path` line in the `System variables` window and click `Edit`.

![](images/path.png)

Then click the `New` button and paste the path to the directory that contains all the essential executable files and tools that are part of JDK 8 into the text field that appears. In our example, this directory is `C:\Program Files\Java\jdk1.8.0_202\bin`.

![](images/new.png)

After that, move the created line to the top of the list by clicking `Move Up` button.

![](images/move-up.png)

Then close the windows by clicking `OK` button.

After setting up the environment variables, verify that Java is installed correctly. Open a command prompt and type the following command to display the Java version on the screen:
Then create the directory for the future Minecraft server. For example, name it `minecraft`:
```
java -version
```
Then create the directory for the future Minecraft server. For example, name it `minecraft`:

You should see output similar to:

![](images/java-version.png)

## Conclusion

So we looked at how to install JDK 8 on Windows Server 2019 and configure the environment variables necessary for the software to function.

