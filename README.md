Role Name
=========

A brief description of the role goes here.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

- vm_name: string
  description: The name of the VM to be actuated.
  required: true

- vm_state: string
  description: The desired state of the VM.
  required: true

- vm_memory: string
  description: The amount of memory to be allocated to the VM - suffixed with GB.
  required: true
  default: 4GB

- vm_cpus: integer
  description: The number of CPUs to be allocated to the VM.
  required: true
  default: 1

- vm_disk_size: string
  description: The size of the disk to be allocated to the VM - suffixed with GB.
  required: true
  default: 10GB

- vm_network_switch: string
  description: The name of the network switch to be used for the VM.
  required: true

- vm_boot_device: string
  description: The boot device to be used for the VM.  Options: Floppy, CD, IDE, LegacyNetworkAdapter, NetworkAdapter, VHD
  required: true
  default: VHD

Dependencies
------------

This depends on the `kenmoini.hyperv` Ansible Collection.

```
ansible-galaxy collection install git+https://github.com/kenmoini/ansible-collection-hyperv.git,main
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
