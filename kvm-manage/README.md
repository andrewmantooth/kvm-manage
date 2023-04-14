# Role Name

- This role will manage vms provided by kvm, including the creation, configuration, and deletion of vms.
- The intent is to require as few vars be set as possible, with the option to customize the role.
  - The default passwords and settings of the image are bad and should be addressed in a follow on 'baseline' ansible role./
- The role will be modular and enable it to be used to make 1-many vms depending on the project, 'studying AAP, Fedora test machine for a new release, etc'

## Requirements

- Machine needs to be capable of being a hypervisor and have libvirt/kvm installed. This can be automated/detected in the future but now the assumption is that it's running on a default Fedora workstation which has the bulk of the deps installed by default.

## Role Variables

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

## Dependencies

- None yet

## Example Playbook

Example playbook creating a VM named 'aap-test' with the default mem, cpu settings

- name: Build AAP lab
  hosts: localhost
  connection: local
  roles:
  - role: kvm-manage
    vms:
    - state: present
      name: aap-test

Example playbook deleting a VM named 'aap-test'.

- name: Shutdown and delete aap-test
  hosts: localhost
  connection: local
  become: true
  roles:
  - role: kvm-manage
    vms:
    - state: absent
      name: "aap-test"

## License

BSD

## Author Information

Andrew is an aging millenial
