# Multi-Node Apache Hadoop 2.7.0 Cluster Setup

The project uses the following technologies:
1. Install Java SDK 8
2. Install Hadoop 2.7.0
3. Install Spark
4. Install SSH Remote Access
5. 
6. Test
7. 

Allocate four 8GBRam/2Core, Ubuntu 14.04 instances in the cloud (use a cloud service provider of your choice).
We called them: master (IP addr: x.y.z.156) slave1 (IP addr: x.y.z.157) and slave2 (IP addr: x.y.z.158).

# Install Java JDK 8
```
$ sudo apt-add-repository ppa:webupd8team/java
$ sudo apt-get update
$ sudo apt-get install -y oracle-java8-installer
```
Check Java Version
```
$ java -version

java version "1.8.0_91"
Java(TM) SE Runtime Environment (build 1.8.0_91-b14)
Java HotSpot(TM) 64-Bit Server VM (build 25.91-b14, mixed mode)
```

# Prepare to Install Hadoop.
### Create user group "hadoop".
```
# sudo addgroup hadoop
Adding group `hadoop' (GID 1000) ...
Done.

# sudo adduser --ingroup hadoop hduser
Adding user `hduser' ...
Adding new user `hduser' (1001) with group `hadoop' ...
Creating home directory `/home/hduser' ...
Copying files from `/etc/skel' ...
Enter new UNIX password: (Keep same on all nodes for convenience)
Retype new UNIX password: 
passwd: password updated successfully
Changing the user information for hduser
Enter the new value, or press ENTER for the default
    Full Name []: 
    Room Number []: 
    Work Phone []: 
    Home Phone []: 
    Other []: 
Is the information correct? [Y/n] Y
```
### Download Hadoop 2.7.0 and extract it to /opt/ directory on All Node
Below are the commands,
```
$ cd /opt/
$ wget http://mirrors.sonic.net/apache/hadoop/common/hadoop-2.7.0/hadoop-2.7.0.tar.gz
$ tar –xvf hadoop-2.7.0.tar.gz
```
### Configure Variables and Reload the Configuration




