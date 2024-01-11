# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2024-01-10

### Added

- Role for setting up a Python virtual environment, for ansible to use
- Role for setting up Docker on a host system, dependent on the above Python role
- Setup automatic deployment to `ansible-galaxy` on `release`.

## [2.0.0] - 2024-01-11

### Added

- Specific dependency for `community.docker` to version `3.6.0-b1` to facilitate use of `docker_compose_v2`
- Obviated the dependency on python and python packages for use of docker
- Improved docker-compose testing with use of a test `docker-compose.yaml`
- Changelog

### Removed

- Python role due to aforementioned obviation of python dependency in `community.docker` collection
- Python package installation in docker installation role
