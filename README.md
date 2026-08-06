# JME Index Type Registry

This repository is the source of truth for the OpenSearch index types used by the JME examples. The build validates
mapping compatibility and publishes a typed Maven artifact for every index type and major version.

## Build

The build requires Java 25.

```bash
./mvnw clean verify
```

For detailed information about the registry format, validation and generated artifacts, see the
[index type registry Maven plugin](https://github.com/jeap-admin-ch/jeap-opensearch-index-type-registry-maven-plugin).

## Note

This repository is part of the [JME open source distribution](https://github.com/jme-admin-ch/jme).

## License

This repository is Open Source Software licensed under the [Apache License 2.0](./LICENSE).
