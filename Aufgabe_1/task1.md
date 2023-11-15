# Task 1
## Task details

* Create an inventory in INI format consisting of
  * A node `localhost` (the ansible-master)
  * A node `schulung[1-15]` (the hostnames of the managed nodes) with the remote host address (ansible_host) `oc-ansible-schulung-[1-15].centralus.cloudapp.azure.com`
  * A group `schulung` that contains the node `schulung[1-15]`.
  * Note: Under comparison with https://docs.ansible.com/ansible/latest/user_guide/intro_inventory.html#list-of-behavioral-inventory-parameters

* Do not use ssh to access localhost, set the host variable `ansible_connection=local` there instead
* Training1 should first authenticate itself with an ssh key, set the host variables there to `~/.ssh/schulung_rsa`.
* Create an ansible config under the Ansible root directory `./ansible.cfg` which initially has no active entries.
  * Create an entry that points to the created inventory.
  * Create an entry so that ansible uses the user `sysadmin` on the target system.
* Execute an ad-hoc command to ping the `schulung` group.
