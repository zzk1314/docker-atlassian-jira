First,you must git clone this repository. then find some resource from google.
 
Such as atlassian-extras-3.2.jar ; mysql-connector-java-5.1.39-bin.jar ; postgresql-9.4.1212.jar ; sources.list.163

Run docker build command to build jira image

```dockerfile
docker run --name jira-db -v jira-volume:/var/lib/mysql \
	-e MYSQL_ROOT_PASSWORD=zzk93615 \
	-e TZ=Asia/Shanghai \
	-e MYSQL_DATABASE=jira \
	-e MYSQL_USER=jira \
	-e MYSQL_PASSWORD=zzk93615 \
	-p 3307:3306 \
	-d mysql \
	--character-set-server=utf8mb4 
```

then 