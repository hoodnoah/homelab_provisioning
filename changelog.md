# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.4.0] - 2024-04-26

- Added role for creation of local borg repository
- Updated timezone role variable names to reflect ansible-lint best practices

## [2.3.0] - 2024-04-23

- Added role to install borgbackup

## [2.2.0] - 2024-04-23

- Added timezone role

## [2.1.5] - 2024-03-27

- Fixed incorrect year in `changelog.md`
- Pinned new `community.docker` dependency now that `docker_compose_v2` is stable

## [2.1.4] - 2024-01-13

- Fixed early exit to permit processing of other tasks subsequent to the `bootstrap_docker` role

## [2.1.3] - 2024-01-13

- Added registration of docker installation to permit early-exit in the event docker has already been verified once in the playbook run

## [2.1.2] - 2024-01-13

### Fixed

- Hid Docker-Compose output to prevent `community.docker.docker_compose_v2` from polluting logs w/ warnings about output parsing

## [2.1.1] - 2024-01-12

### Fixed

- `get_uid_gid` role now sets `PUID` and `PGID` in uppercase, rather than lowercase.

## [2.1.0] - 2024-01-12

### Added

- `get_uid_gid` role for registering the current user's uid, gid into `PUID` and `PGID` facts, respectively.

## [2.0.0] - 2024-01-11

### Added

- Specific dependency for `community.docker` to version `3.6.0-b1` to facilitate use of `docker_compose_v2`
- Obviated the dependency on python and python packages for use of docker
- Improved docker-compose testing with use of a test `docker-compose.yaml`
- Changelog

### Removed

- Python role due to aforementioned obviation of python dependency in `community.docker` collection
- Python package installation in docker installation role

## [1.0.0] - 2024-01-10

### Added

- Role for setting up a Python virtual environment, for ansible to use
- Role for setting up Docker on a host system, dependent on the above Python role
- Setup automatic deployment to `ansible-galaxy` on `release`.
