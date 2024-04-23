# timezone

Sets the time zone of a host.

## Requirements

Per [the docs](https://docs.ansible.com/ansible/latest/collections/community/general/timezone_module.html), SmartOS hosts require the `sm-set-timezone` utility for this role to work.

## Role Variables

`TIME_ZONE`: defaults to `America/New_York`, this is where you set your desired time zone.

## Dependencies

Depends on the [community.general.timezone](https://docs.ansible.com/ansible/latest/collections/community/general/timezone_module.html) module.

## Example Playbook

    - hosts: servers
      roles:
         - { role: hoodnoah.timezone, time_zone: America/Los_Angeles }

## License

MIT

## Author Information

Noah Hood | hood.noah@icloud.com
