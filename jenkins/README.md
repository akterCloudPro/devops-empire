## Jenkins
Jenkins is a self-contained, open source automation server which can be used to automate all sorts of tasks related to building, testing, and delivering or deploying software.

Jenkins can be installed through native system packages, Docker, or even run standalone by any machine with a Java Runtime Environment (JRE) installed.

### Installing Jenkins
```
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
```

#### Jenkins login:
> URL: host ip:8080

> Default Username : admin

> For default Password (run) : cat /var/lib/jenkins/secrets/initialAdminPassword

### Jenkins pipeline implementation (Demo)
> Spring -> Maven -> Jenkins -> Tomcat

![jm](https://user-images.githubusercontent.com/73134659/152977097-7ea7b0fe-65f3-4b42-982a-5234b18caa96.JPG)

