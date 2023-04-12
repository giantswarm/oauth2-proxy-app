# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added

- Add PodDisruptionBudget with `maxUnavailable: "25%"`
- Usage of SeccompProfile in Pod and Container securityContext

### Changed

- Include PodSecurityPolicies only if available. Adds support for Kubernetes 1.25 and higher

## [2.8.0] - 2023-02-01

### Added

- Add support for additional environment variables

### Changed

- Add acme annotation only if letsencrypt is explicitly enabled which should make it possible to use other cert-issuers without having conflicting annotation values

## [2.7.1] - 2022-08-05

## [2.7.0] - 2022-07-19

### Added

- Add support for specifying an existing Secret for provider credentials. Each provider specified in `oauth2Proxy.providers` now supports specifying an existing Secret with fields `cookie-secret`, `client-secret` and `client-id` by setting `oauth2Proxy.providers[].existingSecret` to the name of an existing Secret.

## [2.6.1] - 2022-07-15

### Fixed

- Certain values combinations caused rendering to fail

## [2.6.0] - 2022-04-25

### Added

- Add support for multiple host names

## [2.5.0] - 2022-02-25

### Added

- Add `nameOverride` to values

### Changed

- Upgrade to upstream version [v7.2.1](https://github.com/oauth2-proxy/oauth2-proxy/releases/tag/v7.2.1)
- Add `application.giantswarm.io/team` to default labels

## [2.4.0] - 2021-11-16

### Added

- Ability to configure extra arguments for the oauth2-proxy container per provider (`oauth2Proxy.provider[].extraArgs`)
- Ability to configure extra arguments for the oauth2-proxy container for all providers (`oauth2Proxy.extraArgs`)

### Changed

- Upgrade to upstream version [v7.2.0](https://github.com/oauth2-proxy/oauth2-proxy/releases/tag/v7.2.0)

## [2.3.0] - 2021-11-08

### Changed

- Allow disabling TLS.

## [2.2.4] - 2021-11-04

- Metadata update

## [2.2.3] - 2021-11-03

- Metadata update

## [2.2.2] - 2021-10-15

### Added

- Add icon

### Changed

- Update upstream links in README

## [2.2.1] - 2021-10-04

### Fixed

- Fix lack of quoting on extra annotation values that causes issues for booleans.

## [2.2.0] - 2021-10-01

### Added

- Allow users to add extra annotations to the ingress for services like external-dns.

## [2.1.0] - 2021-10-01

### Added

- Add ingress class support

## [2.0.1] - 2021-09-30

### Fixed

- Fix ingress capability test.

## [2.0.0] - 2021-09-30

### Added

- Add multiple provider support.
- Add ingress for the app.

### Changed

- Rename it to oauth2-proxy
- Include the app in the managed app catalog

## [1.3.0] - 2021-08-10

### Added

- Add `Github` actions.

### Changed

- Migrate to configuration management.
- Update `architect-orb` to v4.0.0.

## [1.2.0] - 2020-05-25

- Use name from values as endpoint selector in service.

## [1.1.1] - 2020-04-27

### Changed

- Changed back namespace from `giantswarm` to `monitoring`.

## [1.1.0] - 2020-04-27

### Changed

- Change chart namespace from `monitoring` to `giantswarm`.

## [1.0.0] - 2020-04-27

### Changed

- Push `g8s-oauth2-proxy` chart into `control-plane` catalog instead of quay.io.
- Push `g8s-oauth2-proxy` app CRs into `<provider>-app-collection` repository.

[Unreleased]: https://github.com/giantswarm/oauth2-proxy-app/compare/v2.8.0...HEAD
[2.8.0]: https://github.com/giantswarm/oauth2-proxy-app/compare/v2.7.1...v2.8.0
[2.7.1]: https://github.com/giantswarm/oauth2-proxy-app/compare/v2.7.0...v2.7.1
[2.7.0]: https://github.com/giantswarm/oauth2-proxy-app/compare/v2.6.1...v2.7.0
[2.6.1]: https://github.com/giantswarm/oauth2-proxy-app/compare/v2.6.0...v2.6.1
[2.6.0]: https://github.com/giantswarm/oauth2-proxy-app/compare/v2.5.0...v2.6.0
[2.5.0]: https://github.com/giantswarm/oauth2-proxy-app/compare/v2.4.0...v2.5.0
[2.4.0]: https://github.com/giantswarm/oauth2-proxy-app/compare/v2.3.0...v2.4.0
[2.3.0]: https://github.com/giantswarm/oauth2-proxy-app/compare/v2.2.4...v2.3.0
[2.2.4]: https://github.com/giantswarm/oauth2-proxy-app/compare/v2.2.3...v2.2.4
[2.2.3]: https://github.com/giantswarm/oauth2-proxy-app/compare/v2.2.2...v2.2.3
[2.2.2]: https://github.com/giantswarm/oauth2-proxy-app/compare/v2.2.1...v2.2.2
[2.2.1]: https://github.com/giantswarm/oauth2-proxy-app/compare/v2.2.0...v2.2.1
[2.2.0]: https://github.com/giantswarm/oauth2-proxy-app/compare/v2.1.0...v2.2.0
[2.1.0]: https://github.com/giantswarm/oauth2-proxy-app/compare/v2.0.1...v2.1.0
[2.0.1]: https://github.com/giantswarm/oauth2-proxy-app/compare/v2.0.0...v2.0.1
[2.0.0]: https://github.com/giantswarm/oauth2-proxy-app/compare/v1.3.0...v2.0.0
[1.3.0]: https://github.com/giantswarm/oauth2-proxy-app/compare/v1.2.0...v1.3.0
[1.2.0]: https://github.com/giantswarm/oauth2-proxy-app/compare/v1.1.1...v1.2.0
[1.1.1]: https://github.com/giantswarm/oauth2-proxy-app/compare/v1.1.0...v1.1.1
[1.1.0]: https://github.com/giantswarm/oauth2-proxy-app/compare/v1.0.0...v1.1.0
[1.0.0]: https://github.com/giantswarm/oauth2-proxy-app/tag/v1.0.0
