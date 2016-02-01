# WSO2 Microservices Server - Parent POM for Microservices

This parent POM file makes life easy for developers who write microservices using WSO2 MSF4J. The following example
from the [stockquote-msf4j-lite](../samples/stockquote-msf4j-lite) microservice example, demonstrates how to quickly write a POM for your microservice using the
MSF4J Service Parent POM.

```xml
<project xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://maven.apache.org/POM/4.0.0"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/maven-v4_0_0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <parent>
        <groupId>org.wso2.msf4j</groupId>
        <artifactId>msf4j-serverless-parent</artifactId>
        <version>1.0.0-SNAPSHOT</version>
        <relativePath>../../msf4j-serverless-parent/pom.xml</relativePath>
    </parent>

    <groupId>org.wso2.msf4j.example</groupId>
    <artifactId>stockquote-msf4j-lite</artifactId>
    <packaging>jar</packaging>

    <name>StockQuote MSF4J Lite</name>
    <name>Executable Jar Microservice Sample</name>

    <properties>
        <microservice.mainClass>org.wso2.msf4j.example.StockQuoteService</microservice.mainClass>
    </properties>
</project>
```

The microservice.mainClass Maven property should be used to define your main class. i.e. the class that includes
the main method.