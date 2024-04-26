# borgrepo_local

Sets up a local borg repository for daily backups of provided directories and/or files.

## Requirements

Must have [`borgbackup`](https://www.borgbackup.org/) installed.
(Note: borgbackup can be installed using the borgbackup role in this collection).

## Role Variables

- `borgrepo_app_name`

  - A string representing the name of the application to be backed up.
    This will be the name of the repository when created.

- `borgrepo_repo_path`
  - The path to the storage location of the repository
    Must be a local filepath.
- `borgrepo_passphrase`
  - The passphrase used to encrypt the borg repository.
- `borgrepo_backup_paths`
  - List of paths to be backed up daily to the borg repository.
    May be a single path, but must still be passed as a list.

## Dependencies

- borgbackup

## Example Playbook

```yaml
- hosts: backup
  roles:
    - role: borgrepo
      vars:
        - borgrepo_app_name: "test"
        - borgrepo_repo_path: "/var/test_backup"
        - borgrepo_passphrase: "test"
        - borgrepo_backup_paths:
            - "/var/test"
```

## License

MIT

## Author Information

Noah Hood [hood.noah@icloud.com](mailto:hood.noah@icloud.com)
