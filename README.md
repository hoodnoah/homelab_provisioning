# Homelab Provisioning Collection

This collection includes Ansible roles for tasks common across hosts for provisioning my homelab.

## Roles

- [bootstrap_docker](roles/bootstrap_docker/README.md): A role for installing/ensuring Docker is installed and operational.
- [python_venv](roles/python_venv/README.md): A role that instantiates a virtual environment for use with Ansible, to permit installation of pip packages without breaking the system install per [PEP 668](https://peps.python.org/pep-0668/).

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
    - python_venv
```

## License

This project is licensed under the MIT License.

## Author

Noah Hood [hood.noah@icloud.com](mailto:hood.noah@icloud.com)
