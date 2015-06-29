# Jade4Ninja

Jade4Ninja(beta) give support for Jade4J for Java templating

Basic functionalities

## Installation


* Add repository

```HTML
    <repositories>
      <repository>
        <id>jade4ninja-repo</id>
        <url>https://raw.github.com/mysu/jade4ninja/mvn-repo/</url>
        <snapshots>
          <enabled>true</enabled>
          <updatePolicy>always</updatePolicy>
        </snapshots>
      </repository>
    <repositories>
```

* Add dependency in pom.xml

```HTML
    <dependency>
      <groupId>org.ninjaframework</groupId>
        <artifactId>jade4ninja</artifactId>
        <version>0.3.0</version>
        <exclusions>
          <exclusion>
            <artifactId>commons-logging</artifactId>
            <groupId>commons-logging</groupId>
          </exclusion>
        </exclusions>
    </dependency>
```
# How to use

* Add the Jade files in _views_ path in the same way that freemaker _.ftl.html_ files. Instead use _.jade_ as the extension
* Reference the _jade4ninja_ module in your in your application
```java
@Singleton
public class Module extends AbstractModule {
    

    protected void configure() {
        
        install(new Jade4NinjaModule());
        
        bind(StartupActions.class);    
        
    }

}
```
* Replace the default system views for `403` and `404` pages in `views/system` with the jade [specific](/jade4ninja-demo/src/main/java/views/system/4043forbidden.jade) [ones](/jade4ninja-demo/src/main/java/views/system/403forbidden.jade)

For more information, see a full usage example in _jade4ninja-demo_



## Reference

* NinjaFramework: www.ninjaframework.org
* Jade4J: https://github.com/neuland/jade4j
