# w2k3_legacy_consul
Repo for the Java Petstore app (legacy) running on a Windows 2003 Server, using Consul sidecar to setup sidecar proxy. 

This repo is to deploy a Windows 2003 Server based on ami-09f348b059878e5f9. 

The AMI is available in us-east-1. It contains the Java Petstore application, J2EE SDK 1.4, and all dependencies for the legacy app to run. 

The J2EE_HOME environment variable should be set, if it is not, it should be: c:\j2sdkee1.3.1
The JAVA_HOME environment variable should be set, if it is not, it should be: c:\j2sdk1.4.2_19

# To start the Java Petstore Application and database, bring up 3 command prompts 

From command prompt 1, run these commands: 

cd "c:\Program Files\petstore1.3.1_02"
setup.bat

From command prompt 2, run these commands:

cd "c:\%J2EE_HOME%"\bin
cloudscape.bat -start

From command prompt 3, run these commands:

cd "c:\%J2EE_HOME%"\bin
j2ee.bat -verbose

Go back to command prompt 1, and run: 
setup.bat deploy. 

This is going to deploy the data to the database. 

Leave these 3 command prompts up and running in the background. 

# Consul

The Consul binary is located in: C:\"Program Files"

To run this binary, cd to the directory, and run it with consul.exe when it is time. 

example:
 C:\ Program Files\>: consul.exe
