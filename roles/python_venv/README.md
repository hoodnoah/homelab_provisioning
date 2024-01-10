# Role Name

Instantiates a virtual environment for use with Ansible, to permit installation of pip packages without breaking the system install per [PEP 668](https://peps.python.org/pep-0668/).

Registers location of `python`, `pip` executables for use with downstream tasks, roles, etc.

## Requirements

None

## Role Variables

- venv_dir
  - default: `/opt/ansible_venv`

## Dependencies

None

## Role Facts

This role sets the following facts:

- `ansible_python_path`: The path to the Python executable in the virtual environment. This fact is set by appending `/bin/python` to the `venv_dir` variable.

- `ansible_pip_path`: The path to the pip executable in the virtual environment. This fact is set by appending `/bin/pip` to the `venv_dir` variable.

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts: all
  roles:
    - role: hoodnoah.python_venv
```

## License

MIT

## Author Information

Noah Hood, [hood.noah@icloud.com](mailto:hood.noah@icloud.com)
