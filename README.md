# ME Binaries

This repository exposes Avro modificated binaries compiled from
[this other git repository][modified-avro].

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

[modified-avro]: https://github.com/geteloquent/avro
