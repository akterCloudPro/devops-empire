## SonarQube
SonarQube® is an automatic code review tool to detect bugs, vulnerabilities, and code smells in your code. It can integrate with your existing workflow to enable continuous code inspection across your project branches and pull requests.

#### Installing and running the local instance of SonarQube as docker container
- > *sudo sysctl -w vm.max_map_count=262144*
- Clone the repository or download the docker-compose.yml file
- Execute the command ** docker-compose up **

##### Running containers
![sonarqube](https://user-images.githubusercontent.com/73134659/152849762-563d047c-a05b-4f9e-8a44-fb6dda9bbb73.JPG)

##### Once the instances are up and running, Log in to http://IP:9000 using System Administrator credentials:
```
login: admin
password: admin
```
![sq](https://user-images.githubusercontent.com/73134659/152848728-c44712c6-8187-4de9-be6a-1448330cc99a.JPG)
