Skeleton playbook
=================

- Contains the structure for creating a playbook following Ansible Best Practice guidelines.
- Contains a basic vagrant setup that can be used for testing ansible / vagrant configuration.

Instructions
------------

Clone the repository:

```
git clone git@github.com:mark-cooper/skeleton-playbook.git
```  

Change to the source directory and run:

```
cp group_vars/all.example group_vars/all
cp vagrant.yml.example vagrant.yml
cp Vagrantfile.example Vagrantfile
# edit the above files as preferred
vagrant up
```

If it fails "GATHERING FACTS" the first time, try:

```
vagrant provision
```

It should successfully create a VM with 512 RAM and run an 'apt-get update' & 'apt-get upgrade' via Ansible.

---
