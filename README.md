# CentOS 7 EPEL7 Repository Install Role

Install or uninstall EPEL7 repository.

That's it, that's all it does.

Some setups require EPEL, others don't so the only way to do it is to make it into a seperate role and install on demand.

Uninstall option also available in case it has to be removed due to conflicts or in favor of other 3rd party repository.

## Requirements

None.

## Role Variables

`INSTALL_EPEL` set to `true` if it needs to be installed.  

`UNINSTALL_EPEL` set to `true` if it needs to be installed, otherwise leave empty.

## Dependencies

None.

## Example Playbook

Fetch this role from Ansible Galaxy:

`ansible-galaxy install mariuszczyz.centos-epel`

In playbook.yml:

```bash
- hosts: servers
  roles:
    - { role: mariuszczyz.centos-epel, tags: ['centos-epel'] }
```

Run it:

`ansible-playbook -i hosts playbook.yml --user root --ask-pass --limit=servers`

Optionally, run just this role:

`ansible-playbook -i hosts playbook.yml --user root --ask-pass --limit=servers --tags=centos-epel`

## License

BSD

## Author Information

Author: Mariusz Czyz  

Date: 09/2018
