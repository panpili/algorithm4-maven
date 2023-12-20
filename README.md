# algorithm4-maven
A maven repo for the [algs4 jar](https://algs4.cs.princeton.edu/code/) of Algorithms 4th class.

## How to use
In pom.xml

```xml

<project>
    <repositories>
        <repository>
            <id>github</id>
            <name>GitHub OWNER Apache Maven Packages</name>
            <url>https://maven.pkg.github.com/panpili/algorithm4-maven</url>
        </repository>
    </repositories> 
    ...
    <dependencies>
        <dependency>
            <groupId>edu.princeton.cs</groupId>
            <artifactId>algs4</artifactId>
            <version>1.0.0</version>
        </dependency>
    </dependencies>
</project>
```

## How to deploy the jar to repository
Follow the [guide](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-apache-maven-registry).
### command
```bash
mvn deploy:deploy-file -DgroupId=edu.princeton.cs \
-DartifactId=algs4 \
-Dversion=1.0.0 \
-Dpackaging=jar \
-Dfile=algs4.jar \
-DrepositoryId=github \
-Durl=https://maven.pkg.github.com/panpili/algorithm4-maven
```
