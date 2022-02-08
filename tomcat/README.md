## Apache Tomcat
Apache Tomcat is an open-source Java servlet and Java Server Page container that lets developers implement an array of enterprise Java applications. Tomcat also runs a HTTP web server environment in which Java code can run.

### Installation procedure
- Install openjdk 8
- wget https://dlcdn.apache.org/tomcat/tomcat-8/v8.5.75/bin/apache-tomcat-8.5.75.tar.gz
- sudo tar --xvzf apache-tomcat-8.5.75.tar.gz
- cd apache-tomcat-8.5.75/bin
- sudo ./startup.sh 

### Access Tomcat 8 admin gui from different host-

> sudo nano tomcat_folder/webapps/host-manager/META-INF/context.xml

*Uncomment Valve section as follows*
```
<Context antiResourceLocking="false" privileged="true" >
  <!--<Valve className="org.apache.catalina.valves.RemoteAddrValve"
         allow="127\.\d+\.\d+\.\d+|::1|0:0:0:0:0:0:0:1" />-->
</Context>
```

### Creating user

**Add desired user and role in tomcat-users.xml file**
```
<role rolename="manager-gui"/>
<user username="akter" password="@kt3r123" roles="manager-gui"/>
```
