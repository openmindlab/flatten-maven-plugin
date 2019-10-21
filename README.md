# MojoHaus Flatten Maven Plugin (forked and published)

This is the just the [flatten-maven-plugin](http://www.mojohaus.org/flatten-maven-plugin/) being forked and published. Waiting for official release...
 
[![Apache License, Version 2.0, January 2004](https://img.shields.io/github/license/mojohaus/versions-maven-plugin.svg?label=License)](http://www.apache.org/licenses/)
[![Maven Central](https://img.shields.io/maven-central/v/org.codehaus.mojo/flatten-maven-plugin.svg?label=Maven%20Central)](http://search.maven.org/#search%7Cga%7C1%7Cflatten-maven-plugin)
[![Build Status](https://travis-ci.org/mojohaus/flatten-maven-plugin.svg?branch=master)](https://travis-ci.org/mojohaus/flatten-maven-plugin)
1.0.x branch: [![Build Status 1.0.x](https://travis-ci.org/mojohaus/flatten-maven-plugin.svg?branch=1.0.x)](https://travis-ci.org/mojohaus/flatten-maven-plugin)

## Quickstart
This plugin generates a flattened version of your pom.xml and makes maven to install and deploy this one instead of the original pom.xml.
```
  <build>
    <plugins>
      <plugin>
        <groupId>net.sourceforge.openutils</groupId>
        <artifactId>flatten-maven-plugin</artifactId>
        <!--<version>INSERT LATEST VERSION HERE</version>-->
        <executions>
          <execution>
            <goals>
              <goal>generate</goal>
            </goals>
          </execution>
        </executions>
        <configuration>
          <!-- See usage on maven site from link above for details -->
        </configuration>
      </plugin>
    </plugins>
  </build>
```

## Releasing

* Make sure `gpg-agent` is running.
* Execute `mvn -B release:prepare release:perform`

For publishing the site do the following:

```
cd target/checkout
mvn verify site site:stage scm-publish:publish-scm
```
