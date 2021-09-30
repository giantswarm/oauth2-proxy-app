# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added

- Add multiple provider support.
- Add ingress for the app.

### Changed

- Rename it to oauth2-proxy-app
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

[Unreleased]: https://github.com/giantswarm/oauth2-proxy-app/compare/v1.3.0...HEAD
[1.3.0]: https://github.com/giantswarm/oauth2-proxy-app/compare/v1.2.0...v1.3.0
[1.2.0]: https://github.com/giantswarm/oauth2-proxy-app/compare/v1.1.1...v1.2.0
[1.1.1]: https://github.com/giantswarm/oauth2-proxy-app/compare/v1.1.0...v1.1.1
[1.1.0]: https://github.com/giantswarm/oauth2-proxy-app/compare/v1.0.0...v1.1.0
[1.0.0]: https://github.com/giantswarm/oauth2-proxy-app/tag/v1.0.0
