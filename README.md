# aap-hub

Project to deploy aap and private hub on kvm

- KVM automation stolen from https://www.redhat.com/sysadmin/build-VM-fast-ansible
- Will result in a vm with a both a root and power user (devops) with passwords set. However, only the root ssh key is currently working :/

TODO:

- Add rhel local image bit
  - Make rhel bit a seperate block which only runs if called
- Add a bit to kill all vms?
- Make follow up role?
- Make the image with packer?
