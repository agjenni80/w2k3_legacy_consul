# w2k3_legacy_consul
Repo for the Java Petstore app (legacy) running on a Windows 2003 Server, using Consul sidecar to setup sidecar proxy. 

This repo is to deploy a Windows 2003 Server based on ami-09f348b059878e5f9. 

The AMI is available in us-east-1. It contains the Java Petstore application, J2EE SDK 1.4, and all dependencies for the legacy app to run. 

# To start the Java Petstore Application and database. 

From a command prompt: 

cd "c:\Program Files\petstore1.3.1_02"

Run setup.bat

Bring up a new command prompt:

cd "c:\%J2EE_HOME%"\bin

Run cloudscape.bat -start


Bring up a new command prompt:

cd "c:\%J2EE_HOME%"\bin

run j2ee.bat -verbose


# Leave these 3 command prompts up and running in the background. 


