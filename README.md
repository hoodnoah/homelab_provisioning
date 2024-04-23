# Homelab Provisioning Collection

This collection includes roles which are common tasks across many hosts on my homelab, namely the bootstrapping of Docker, since substantially all the services on my homelab are containerized.

## Roles

- [bootstrap_docker](roles/bootstrap_docker/README.md): A role for installing/ensuring Docker is installed and operational.
- [get_uid_gid](roles/get_uid_gid/README.md): A role for collecting the current user's UID and GID, for injection into [Linuxserver's Docker-Compose images](https://docs.linuxserver.io/general/understanding-puid-and-pgid/).
- [timezone](roles/timezone/README.md): A role for setting the timezone. Defaults to "America/New_York".
- [borgbackup](roles/borgbackup/README.md): A role for installing [borgbackup](https://www.borgbackup.org).

## Requirements

- Ansible 2.1 or higher

## Installation

To install this collection, use the `ansible-galaxy` command:

```bash
ansible-galaxy collection install hoodnoah.homelab_provisioning
```

## Usage

```yaml
- hosts: all
  collections:
    - hoodnoah.homelab_provisioning
  roles:
    - bootstrap_docker
    - timezone
    - borgbackup
```

## License

This project is licensed under the MIT License.

## Author

Noah Hood [hood.noah@icloud.com](mailto:hood.noah@icloud.com)
