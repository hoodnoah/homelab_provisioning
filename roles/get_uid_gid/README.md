# Role Name

Collects the UID, GID of the current user, storing them in the facts `PUID` and `PGID`, respectively.

## Facts

- `puid`: The UID of the current user.
- `pgid`: The GID of the current user.

## Requirements

None.

## Role Variables

None.

## Dependencies

None.

## Example Playbook

    - hosts: servers
      roles:
         - { role: hoodnoah.homelab_provisioning.get_uid_gid }

## License

MIT

## Author Information

Noah Hood [hood.noah@icloud.com](mailto:hood.noah@icloud.com)
