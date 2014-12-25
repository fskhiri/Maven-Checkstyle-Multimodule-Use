Maven-Checkstyle-Multimodule-Use
================================

Maven Checkstyle Plugin Multimodule demo

You can see the project at

http://maven.apache.org/plugins/maven-checkstyle-plugin/examples/multi-module-config.html

and I give the source code :)

Requires 
===

Maven 3.2.1

Eclipse 4.4.1

Google Checkstyle rule

maven-checkstyle-plugin 2.13

Other
===

I got the error

[ERROR] Failed to execute goal org.apache.maven.plugins:maven-site-plugin:3.3:site (default-site) on project whizbang: Error during page generation: Error rendering Maven report: Failed during checkstyle configuration: cannot initialize module TreeWalker - Unable to instantiate AvoidEscapedUnicodeCharacters: Unable to instantiate AvoidEscapedUnicodeCharactersCheck -> [Help 1]

I solved it by config 

```
<dependency>
    <groupId>com.puppycrawl.tools</groupId>
    <artifactId>checkstyle</artifactId>
    <version>6.1.1</version>
</dependency>
```

And this answer helps me a lot

http://stackoverflow.com/questions/27345241/error-using-checkstyle-google-checks-xml-with-maven-checkstyle-plugin
