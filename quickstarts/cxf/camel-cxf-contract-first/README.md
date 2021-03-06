camel-cxf-contract-first: Demonstrates how to create a SOAP Web service
======================================================
Author: Fuse Team  
Level: Beginner  
Technologies: Camel, CXF, SOAP  
Summary: This quickstart demonstrates creating a SOAP Web service in contract first style with Apache CXF and Camel and exposing it through the OSGi HTTP Service.  
Target Product: Fuse  
Source: <https://github.com/jboss-fuse/fuse-karaf/tree/master/quickstarts>  

We are using contract first style, which means the web service is defined in a `.wsdl` file, and then the source code is generated. The web service is then exposed as an endpoint in a Camel route.


What is it?
-----------

This quickstart demonstrates creating a SOAP Web service in contract first style with Apache CXF and Camel and exposing it through the OSGi HTTP Service. 
We are using contract first style, which means the web service is defined in a `.wsdl` file, and then the source code is generated. The web service is then exposed as an endpoint in a Camel route.


System requirements
-------------------

Before building and running this quick start you need:

* Maven 3.3.1 or higher
* JDK 1.8
* JBoss Fuse 7


Build and Deploy the Quickstart
-------------------------

1. Change your working directory to `camel-cxf-contract-first` directory.
2. Run `mvn clean install` to build the quickstart.
3. Start JBoss Fuse 7 by running bin/fuse (on Linux) or bin\fuse.bat (on Windows).
4. In the JBoss Fuse console, enter the following command:

        bundle:install -s mvn:org.jboss.fuse.quickstarts/cxf-camel-cxf-contract-first/${project.version}

5. Fuse should give you an id when the bundle is deployed

6. You can check that everything is ok by issuing  the command:

        bundle:list
   your bundle should be present at the end of the list


Use the bundle
---------------------

To use the application be sure to have deployed the quickstart in Fuse as described above. 

1. cd to the 'camel-cxf-contract-first' directory
2. Run 'mvn -Ptest test'

Or open 'http://localhost:8181/cxf/' in a browser to see 'OrderEndpoint' listed as a SOAP service.

Undeploy the Archive
--------------------

To stop and undeploy the bundle in Fuse:

1. Enter `bundle:list` command to retrieve your bundle id
2. To stop and uninstall the bundle enter

        bundle:uninstall <id>
