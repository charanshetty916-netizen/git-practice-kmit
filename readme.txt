org.apache.maven 

FROM tomcat:9.0
COPY target/ch.war /usr/local/tomcat/webapps/charan.war
EXPOSE 8080
CMD ["catalina.sh","run"]

-----------------------------------------------------------------------------------------

git init
git add .
git config --global user.name name
git config --global user.name name

git commit -m "inintal"
git remote -v

git remote add origin "url"
git push -u origin master

docker built -t myapp .
docker run -p 7012:8080 myapp
docker images

docker login
docker tag myapp:latest username/myapp:latest
docker tag myapp:latest username/myapp:latest

for java prokect 
CITB
clean
install
test
build


For java app
Dockerfile
FROM redis:latest
CMD ["redis-server"]


docker build -t imgname .
docker images
docker run --name credis imgname

docker run -d --name credis imgname
docker logs credis

docker run --name credis uname/imgname:latest


<?xml version="1.0" encoding="UTF-8"?>

<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
  <modelVersion>4.0.0</modelVersion>

  <groupId>google.com</groupId>
  <artifactId>charan</artifactId>
  <version>0.0.1-SNAPSHOT</version>
  <packaging>war</packaging>

  <name>charan Maven Webapp</name>
  <!-- FIXME change it to the project's website -->
  <url>http://www.example.com</url>

  <properties>
    <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
    <maven.compiler.source>8</maven.compiler.source>
    <maven.compiler.target>8</maven.compiler.target>
  </properties>

  <dependencies>
    <dependency>
      <groupId>junit</groupId>
      <artifactId>junit</artifactId>
      <version>4.13.1</version>
      <scope>test</scope>
    </dependency>
  </dependencies>

  <build>
    <finalName>charan</finalName>
    <pluginManagement><!-- lock down plugins versions to avoid using Maven defaults (may be moved to parent pom) -->
      <plugins>
        <plugin>
          <artifactId>maven-clean-plugin</artifactId>
          <version>3.4.0</version>
        </plugin>
        <!-- see http://maven.apache.org/ref/current/maven-core/default-bindings.html#Plugin_bindings_for_war_packaging -->
        <plugin>
          <artifactId>maven-resources-plugin</artifactId>
          <version>3.3.1</version>
        </plugin>
        <plugin>
          <artifactId>maven-compiler-plugin</artifactId>
          <version>3.13.0</version>
        </plugin>
        <plugin>
          <artifactId>maven-surefire-plugin</artifactId>
          <version>3.3.0</version>
        </plugin>
        <plugin>
          <artifactId>maven-war-plugin</artifactId>
          <version>3.4.0</version>
        </plugin>
        <plugin>
          <artifactId>maven-install-plugin</artifactId>
          <version>3.1.2</version>
        </plugin>
        <plugin>
          <artifactId>maven-deploy-plugin</artifactId>
          <version>3.1.2</version>
        </plugin>
      </plugins>
    </pluginManagement>
  </build>
</project>

<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
  <modelVersion>4.0.0</modelVersion>
  <groupId>myjavaproject</groupId>
  <artifactId>java-project</artifactId>
  <version>0.0.1-SNAPSHOT</version>
</project>

Here are all the Git commands from the assignment, scenario by scenario:

**a) First commit on an un-versioned folder**
```
cd railway-ticket-booking
git init
git add .
git commit -m "Initial commit"
```

**b) New feature branch (train search)**
```
git checkout main
git pull origin main
git checkout -b feature/train-search
git add .
git commit -m "Add train search by source and destination"
git push -u origin feature/train-search
```

**c) Review changes before committing**
```
git status
git diff
git add -A
git diff --staged
```

**d) Discard uncommitted changes**
```
git restore train-search.html
# or classic equivalent:
git checkout -- train-search.html
```

**e) Move branch back to an earlier commit (unpushed)**
```
git log --oneline
git reset --hard <commit-hash>
```

**f) Find and delete unused branches**

```
git branch --merged main
git branch -d old-feature
git push origin --delete old-feature
```

**g) Merge two feature branches into main**
```
git checkout main
git pull origin main
git merge feature/train-search
git merge feature/passenger-registration
git add .
git commit -m "Merge train-search and passenger-registration into main"
git push origin main
```

**h) Create, inspect, and apply a patch**
```
git format-patch -1 <commit-hash>
git apply --stat 0001-add-search.patch
git apply --check 0001-add-search.patch
git am 0001-add-search.patch
```

**i) Patch fails to apply cleanly (conflicts)**
```
git apply --reject 0001-add-search.patch
# fix the .rej hunks manually, or use:
git am --3way
git add <resolved-files>
git am --continue
```

**j) Configure remote and push project history**

```
git remote add origin https://github.com/<username>/railway-ticket-booking.git
git branch -M main
git push -u origin main
```
