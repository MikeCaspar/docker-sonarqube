# docker-sonarqube


It can run as a standalone temporary server using h2 (default) or it can be run as a local server with data stored elsewhere. (ie: aws).

Start (default) (set memory to where you need it)

```
docker run -d -m 512m --name sonarqube -p 9000:9000 mikecaspar/docker_sonarqube
```

Start (external db)

```
docker run -d -m 1G --name sonarqube 
--env SONARQUBE_JDBC_USERNAME=xxxxxx 
--env SONARQUBE_JDBC_PASSWORD=xxxxxxxxx 
--env SONARQUBE_JDBC_URL=jdbc:postgresql://<server>:5432/<database> 
-p 9000:9000 
mikecaspar/docker_sonarqube
```

**SonarQube**

[http://www.sonarqube.org/](http://www.sonarqube.org/)
 

**Version History**

Initial Release - 1.0 on Jan 12, 2016
