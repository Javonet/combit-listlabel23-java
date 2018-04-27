# Introduction
Strongly-typed wrapper for combit .NET List &amp; Label component combit.ListLabel23.dll. This project allows you to compile the Jar package which replicates the interface of combit List & Label 23 component so it can be used from Java.

The usage of .NET UI combit component from Java is possible thanks to the usage of thrd-party Javonet library.

This wrapper is used by sample projects available in [Combit Java Samples Repository](https://github.com/Javonet/combit). 

# Contents
Source code includes a strongly typed wrapper project for the combit List & Label .NET component. Strongly-typed wrapper replicates List & Label 23 .NET API for Java. Currently it exposes only the key operations required by sample projects:

- using a List & Label .NET Dataprovider to connect to an Access database with OleDB and respond to an event of the Dataprovider
- calling/opening the List & Label Designer; including real data preview
- printing into the List & Label preview control on the form and respond to a preview control button click event
- exporting into any of the supported List & Label export formats

You can further extend this wrapper to expose the strongly typed methods with signatures matching the combit List & Label .NET component (see also the .NET help at https://docu.combit.net/en) and forwarding the calls via Javonet. To learn more how to perform different types of calls from Java to .NET API using Javonet, go to Javonet Guides for Java developers (https://www.javonet.com/java-devs/guides/).

# How to Open this Project in Eclipse
In this section you will find step by step guide how to open this project. 

1) **Clone this repository** - navigate with console window to the folder where you want to clone the repository and run the command below. Sample source code will be download to **combit-listlabel23-java** folder.
```
git clone https://github.com/Javonet/combit-listlabel23-java.git
```
2) Open **Eclipse IDE**.
> Because by default the source in the repository does not include Eclipse project files you need to create new workspace and import the project.
3) **Create Eclipse Workspace** in the **combit-listlabel23-java** folder created by git.
4) Right click on Project Explorer and choose **Import** next **General** > **Projects from Folder or Archive** and press **Next**.
5) Press **Directory...** and point to the **combit.ListLabel23** within the **combit-listlabel23-java** folder. Wrapper project should be automatically detected. Press **Finish** to complete.
> Now your project is ready, you only need to add missing dependencies.
6) Register for free trial Javonet key [Signup for Javonet](https://my.javonet.com/signup?type=free).
7) After registration is completed download **Javonet JAR** and copy to the Eclipse project.
8) Right click **Javonet Jar** in Eclipse Project Explorer and choose **Build Path** > **Add to Build Path**

Now you can work to extend this wrapper with additional features.

# Extending Strongly-Typed Wrapper
The combit.listlabel23 project replicates the List & Label 23 .NET API in Java and routes the calls through Javonet to the .NET component implementation. This wrapper has been implement to expose only the functionality required for the sample applications. If you need any additional features from List & Label component you should extend this wrapper.

To learn more how to use Javonet to perform different operations on .NET component go to Javonet guide for Java developers: 
https://www.javonet.com/java-devs/guides/

## Compiling Strongly-Typed Wrapper
Once you extend the wrapper with required features you should run the ready to use **build_script.xml** as Ant script to compile the new Jar file. To recompile the wrapper in **Eclipse** follow these steps:
1) Right click the **build_script.xml** choose **Run As** > **Ant Build**
2) Copy the **combit.ListLabel23.jar** from **target** folder to the your application
3) Use your new features…

# Using Wrapper in Your Project
To use this wrapper in your Java application you need to copy compiled Jar of this wrapper from **target** folder, the .NET assembly combit.ListLabel23.dll and Javonet Jar package to your Java application folder. You need also to add both Jars to build path. Make sure to get the latest Javonet Jar package for Java developers and trial or commercial license key from Javonet. To get the sample working, set your licensing information for activating Javonet by calling **ListLabelActivation.setLicense("your@mail.com", "your-license-key");**. 

You can register for Javonet free trial and access download page by registering here (https://my.javonet.com/signup/?type=free).

To get List & Label component register for free trial [Register for combit](https://www.combit.net/en/download-trial/). Next, download and install **combit List & Label** components and copy **combit.ListLabel23.dll** to your Java project root folder.
> combit.ListLabel23.dll can be found in List & Label install directory by default **C:\Program Files (x86)\combit\LL23\Redistributable Files\combit.ListLabel23.dll**. Once this is done you can run your application

# Contribute
This wrapper is maintained and extended by **Javonet** and **combit** developers. Additional methods covering further parts of List & Label API will be added soon. If you cover some critical parts of the API and would like to share your work with others, feel free to create a pull request to this repository and we will be happy to merge your contribution!
