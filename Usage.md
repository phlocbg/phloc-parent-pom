# Introduction #

phloc-parent-pom is a parent POM for [Maven 3.0.4](http://maven.apache.org) and Java 1.6. It offers integration into m2eclipse for some plugins.

Include it as follows in your application in case you checked out this projects trunk in the directory "phloc-parent-pom":
```
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/maven-v4_0_0.xsd">
  <parent>
    <groupId>com.phloc</groupId>
    <artifactId>parent-pom</artifactId>
    <version>22.7</version>
    <relativePath>../phloc-parent-pom/pom.xml</relativePath>
  </parent>
  ...
</project>
```

Note: please adopt the version number and the relativePath to your needs!