## Apache Tomcat

### Access Tomcat 8 admin gui from different host-
> sudo nano tomcat_folder/webapps/host-manager/META-INF/context.xml

```
<Context antiResourceLocking="false" privileged="true" >
  <!--<Valve className="org.apache.catalina.valves.RemoteAddrValve"
         allow="127\.\d+\.\d+\.\d+|::1|0:0:0:0:0:0:0:1" />-->
</Context>
```
