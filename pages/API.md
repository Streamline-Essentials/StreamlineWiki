### Table of Contents:
> * [**Requirements**](#requirements)
> * [**Repositories**](#repositories)
> * [**Dependencies**](#dependencies)
> * [**Deeper Dive**](#deeper-dive)

# Requirements
* You will need to have basic programming knowledge.
* Use Java 11 for backwards compatibility.
* I would recommend using IntelliJ IDEA for development.
  * This tutorial will be using IntelliJ IDEA.

# Repositories
### Gradle
```groovy
repositories {
    mavenCentral()
    maven { url = 'https://oss.sonatype.org/content/repositories/snapshots' }
    maven { url = 'https://oss.sonatype.org/content/repositories/central' }
    maven { url = 'https://jitpack.io' }
}
```
### Maven
```xml
<repositories>
    <repository>
        <id>sonatype-snapshots</id>
        <url>https://oss.sonatype.org/content/repositories/snapshots</url>
    </repository>
    <repository>
        <id>sonatype-central</id>
        <url>https://oss.sonatype.org/content/repositories/central</url>
    </repository>
    <repository>
        <id>jitpack.io</id>
        <url>https://jitpack.io</url>
    </repository>
</repositories>
```

# Dependencies
### Gradle
Main Core:
```groovy
dependencies {
  compileOnly "net.luckperms:api:5.4"

  compileOnly("com.github.Streamline-Essentials.StreamlineCore:StreamlineCore-API:main-SNAPSHOT")
  annotationProcessor("com.github.Streamline-Essentials.StreamlineCore:StreamlineCore-API:main-SNAPSHOT")
}
```

Spigot Core (for development with Spigot):
###### Note: The Spigot Core has the Main Core inside it (so you don't need to add the Main Core as a dependency).
```groovy
dependencies {
    compileOnly "net.luckperms:api:5.4"

    compileOnly("com.github.Streamline-Essentials.StreamlineCore:StreamlineCore-BAPI:main-SNAPSHOT")
    annotationProcessor("com.github.Streamline-Essentials.StreamlineCore:StreamlineCore-BAPI:main-SNAPSHOT")
}
```
### Maven
Main Core:
```xml
<dependencies>
    <dependency>
        <groupId>net.luckperms</groupId>
        <artifactId>api</artifactId>
        <version>5.4</version>
        <scope>provided</scope>
    </dependency>
    <dependency>
        <groupId>com.github.Streamline-Essentials.StreamlineCore</groupId>
        <artifactId>StreamlineCore-API</artifactId>
        <version>main-SNAPSHOT</version>
        <scope>provided</scope>
    </dependency>
</dependencies>
```

Spigot Core (for development with Spigot):
###### Note: The Spigot Core has the Main Core inside it -- so you don't need to add the Main Core as a dependency.
```xml
<dependencies>
    <dependency>
        <groupId>net.luckperms</groupId>
        <artifactId>api</artifactId>
        <version>5.4</version>
        <scope>provided</scope>
    </dependency>
    <dependency>
        <groupId>com.github.Streamline-Essentials.StreamlineCore</groupId>
        <artifactId>StreamlineCore-BAPI</artifactId>
        <version>main-SNAPSHOT</version>
        <scope>provided</scope>
    </dependency>
</dependencies>
```
# Deeper Dive
* Clone the ``ExampleModule`` repository from [here](https://github.com/Streamline-Essentials/ExampleModule).
* More will be added later!
