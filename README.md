bukkit-plugin-parent-pom
===

[![Dependabot Status](https://api.dependabot.com/badges/status?host=github&repo=timbru31/bukkit-plugin-parent-pom)](https://dependabot.com)
[![Known Vulnerabilities](https://snyk.io/test/github/timbru31/bukkit-plugin-parent-pom/badge.svg)](https://snyk.io/test/github/timbru31/bukkit-plugin-parent-pom)

A maven parent POM for all my Bukkit/Spigot plugins.

## What's included

### Dependencies

* Bukkit
* bStats
* Kotlin
* Lombok
* FindBugs Annotations
* JUnit 5
* Mockito
* Hoverfly

### Plugins

* Checkstyle
* PMD
* SpotBugs (+ Find Security Bugs & fb-contrib)

### Profiles

* metrics - this profile shades bStats into the plugin
* kotlin - this profile adds the necessary configuration and shading for Kotlin usage

## Configuration

### Mandatory

* *plugin.name* - your desired plugin name (e.g. MyAwesomePlugin)
* *plugin.main* - the main class used in the plugin.yml (e.g. com.mydomain.pluginMain)
* *plugin.package* - the used plugin package (e.g. com.mydomain)

### Optional

* Bukkit Version (*bukkit.version*), default will stick to the latest available one.
* JDK Version (*jdk.version*), default is *1.8*
* Enforced Maven version (*enforcer.maven.version*), default is *[3,2)*
* Checkstyle ruleset (*checkstyle.location*), default is *https://dustplanet.de/checkstyle.xml*

For further properties, please take a look into the *properties* section of this `pom.xml`.

## Usage

Include the following in your `pom.xml`:

```xml
  <parent>
    <groupId>de.dustplanet</groupId>
    <artifactId>bukkit-plugin</artifactId>
    <version>5.4.10</version>
    <relativePath />
  </parent>

  <properties>
    <plugin.name>MyPlugin</plugin.name>
    <plugin.main>de.dustplanet.myplugin.MyPlugin</plugin.main>
    <plugin.package>de.dustplanet.myplugin</plugin.package>
  </properties>

  <repositories>
    <repository>
      <id>parent</id>
      <url>https://repo.dustplanet.de/artifactory/bukkit-plugins/</url>
    </repository>
  </repositories>
```

---
Built by (c) Tim Brust and contributors. Released under the MIT license.
