![CNPG Extensions](./cnpg-extensions.png)

# CNPG Extensions

A complementary catalog of PostgreSQL extension container images for
[CloudNativePG](https://cloudnative-pg.io/), packaging extensions not already
provided by [upstream](https://github.com/cloudnative-pg/postgres-extensions-containers).

## Why does this exist?

We offer a very wide selection of PostgreSQL extensions for CNPG users through
Debian packages, Rust-based PGRX builds, and Universe source builds. We welcome both extensions outside
upstream's licensing policy and extensions eligible for future upstream inclusion;
prior upstream rejection is not required.

Inclusion follows a
[Debian-first policy](https://github.com/cnpg-extensions/postgres-extensions-containers/blob/main/source-build/README.md#inclusion-policy-debian-packaging-first):
ordinary extensions should be packaged for Debian. PGRX source builds address a
shared toolchain obstacle; Universe source builds require documented complex
dependency packaging or delivery obstacles.

All distributed material must meet the
[Open Source Licensing Policy](https://github.com/cnpg-extensions/postgres-extensions-containers/blob/main/source-build/README.md#open-source-licensing-policy):
OSI-approved terms or prior acceptance and shipment in Debian's `main` or
`contrib` under the same applicable terms, unless maintainers explicitly approve
and document an exception. Exceptions face a high bar and are unlikely.
Applicable license obligations must always be met.

Repository maintainers maintain all extensions. See the
[extension requirements](https://github.com/cnpg-extensions/postgres-extensions-containers#extension-requirements)
for compatibility, dependency evidence, and contribution guidance.

## Repositories

| Repository | Description |
|---|---|
| [postgres-extensions-containers](https://github.com/cnpg-extensions/postgres-extensions-containers) | Debian-packaged, PGRX, and Universe extension images for CloudNativePG |
| [artifacts](https://github.com/cnpg-extensions/artifacts) | Official `ClusterImageCatalog` manifests and signatures for the extension images |
| [cnpg-sbom-generator](https://github.com/cnpg-extensions/cnpg-sbom-generator) | Standalone BuildKit SBOM generator for PostgreSQL extension containers |
| [.github](https://github.com/cnpg-extensions/.github) | Organization profile and README |

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
