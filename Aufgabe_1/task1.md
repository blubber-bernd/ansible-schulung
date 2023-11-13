# Task 1
## Task details

* Create an INI inventory in `./inventory/hosts` consisting of
  * A node `localhost` (the ansible-master)
  * A node `training1` and `node2` (the hostnames of the managed nodes)
  * A group `training` that contains both nodes `node1` and `node2
  * Note: Under comparison with https://docs.ansible.com/ansible/latest/user_guide/intro_inventory.html#list-of-behavioral-inventory-parameters

* Do not use ssh to access localhost, set the host variable `ansible_connection=local` there instead
* the user sysadmin should first authenticate itself with the generated ssh keys, set the host variables `./id_rsa` (for node2 change the path to node2)
* Create an ansible config under `./ansible.cfg` which initially has no active entries.
  * Create an entry that points to the created inventory.
  * Create an entry so that ansible uses the user `sysadmin` on the target system.
* Execute an ad-hoc command to ping the training host.
