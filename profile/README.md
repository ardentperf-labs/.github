![CNPG Extensions](./cnpg-extensions.png)

# CNPG Extensions

A complementary catalog of PostgreSQL extension container images for
[CloudNativePG](https://cloudnative-pg.io/), packaging extensions not already
provided by [upstream](https://github.com/cloudnative-pg/postgres-extensions-containers).

## Why does this exist?

CNPG Extensions broadens the range of extensions available to CNPG users through
Debian packages and Rust-based PGRX builds. We welcome both extensions outside
upstream's licensing policy and extensions eligible for future upstream inclusion;
prior upstream rejection is not required.

Inclusion requires useful functionality within CNPG, current platform support,
transparent and maintainable dependencies, redistribution rights and license
notices, and a committed maintainer. See the authoritative
[extension inclusion policy](https://github.com/cnpg-extensions/postgres-extensions-containers#extension-requirements)
for build routes and release requirements.

## Repositories

| Repository | Description |
|---|---|
| [postgres-extensions-containers](https://github.com/cnpg-extensions/postgres-extensions-containers) | Debian-packaged and PGRX extension images for CloudNativePG |
| [artifacts](https://github.com/cnpg-extensions/artifacts) | Official `ClusterImageCatalog` manifests and signatures for the extension images |

## Usage

See the
[postgres-extensions-containers README](https://github.com/cnpg-extensions/postgres-extensions-containers#readme)
and each extension's directory for `Cluster` and `Database` YAML examples.

## Relationship to upstream

This org tracks the upstream build infrastructure as closely as possible and
continually incorporates upstream improvements. Upstream takes precedence: when
an extension is added upstream, we remove local packaging in favor of the
upstream-maintained image. Our generated catalog retains upstream definitions
and adds extensions maintained here.

A separate **cnpg-universe** catalog for externally maintained images is
[planned](https://github.com/cnpg-extensions/postgres-extensions-containers/issues/290).
Its inclusion and maintenance policies remain to be defined; it is not yet an
available submission route.
