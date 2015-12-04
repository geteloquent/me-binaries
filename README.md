# ME Binaries

This repository exposes Avro modificated binaries compiled from
[this other git repository][modified-avro]. Modified binaries are now exposed as
version 1.9.1-SNAPSHOT. This is true only to the artifacts which were modified:

- avro-compiler
- avro-maven-plugin

### Depend on it

If you want to try out the modified binaries, that's the pom snippet you were
looking for:

```xml
<repositories>
  <repository>
    <id>avro-mvn-repo</id>
    <url>https://raw.github.com/geteloquent/me-binaries/avro/</url>
    <snapshots>
      <enabled>true</enabled>
      <updatePolicy>always</updatePolicy>
    </snapshots>
  </repository>
</repositories>
```

Note: `<repositories>` and `<repository>` tags could be changed for
`<pluginRepositories>` and `<pluginRepository>` as you wish.

Do not forget modifying depencies on avro-maven-plugin and / or avro-compiler to
modified version. For instance:

```xml
<dependency>
  <groupId>org.apache.avro</groupId>
  <artifactId>avro-compiler</artifactId> <!-- or avro-maven-plugin -->
  <version>1.9.1-SNAPSHOT</version>
</dependency>
```

[modified-avro]: https://github.com/geteloquent/avro
