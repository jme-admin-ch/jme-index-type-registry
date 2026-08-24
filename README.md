# JME Index Type Registry

This repository is the source of truth for the OpenSearch index types used by the JME examples. The build validates
mapping compatibility and publishes a typed Maven artifact for every index type and major version.

## Structure

Index types live under `index-types/jme/<index-type>/`, each with a top-level `.json` descriptor and one
`_mapping_v<major>_<minor>.json` OpenSearch mapping file per published version:

- `jmedecree`, `jmedecreedocument`, `jmediagram` — single-version index types.
- `jmetransitdocument` — versioned across `v1_0` to `v1_3`, showing minor-version mapping evolution.
- `jmetransitdecision` — versioned across `v1_0` and `v2_0`, showing major-version mapping evolution.

See `schema/README.md` for the descriptor/mapping file format.

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
