# aap-hub

Project to deploy aap and private hub on kvm

- Will result in a vm with a both a root and power user (devops) with passwords set. However, only the root ssh key is currently working :/

TODO:

- Add rhel local image bit
- Make follow up role baselining role
- Make the image with packer (libvirt is not fully supported as a provider att)

CREDIT:

- KVM automation idea from: https://www.redhat.com/sysadmin/build-VM-fast-ansible
- More modular approach to the role insipred by: https://github.com/stackhpc/ansible-role-libvirt-vm
