# Task 2
This exercise builds on the results of the inventory and ansible.cfg from day 2.

## Goal to achive
At the end of this exercise you should have installed a web server on Ubuntu and be able to reach it with your browser on port 8080.
http://oc-ansible-schulung-[1-15].centralus.cloudapp.azure.com:8080

## Task details
* Copy this result from task 1 into a new folder or use the existing folder you used yesterday again
* Create the roles folder with the role `webserver` in your Ansible project directory
* Create a role for `os_base` komponents.
  * The tasks of this role should Update all packages and also install the package `unzip`
* Create a playbook in the correct location that calls this roles.
  * use the existing `schulung` group as the target vm
* Write tasks/logic in the role `webserver`.
  * The webserver (in Ubuntu its the package name `apache2`) should be installed using the packagemanager.
  * Download the static website from the following link: https://github.com/schwenne/website/archive/refs/tags/v0.0.1.tar.gz
  * Unzip the website and copy it into the folder `/var/www/html` (at the end the folder /var/www/html should contain a file `index.html` and another folder `images`)
  * Change the port for the web server to port `8080` (path: /etc/apache2/ports.conf)
  * Restart or reload the server to activate the configuration
* Use variables in suitable places in the entire Ansible project environment.
  * Tip: There is no right or wrong here. It is best to use variables if the value occurs frequently or if you want it to be easier to change later.
  * Tip2: The webserver port is probably a suitable candidate.
  * Tip3: Try to use the folder group_vars (https://docs.ansible.com/ansible/2.8/user_guide/playbooks_best_practices.html#directory-layout)
* (Optional) If possible, create suitable default values for the set variables


## Tips
Most of the tasks have already been shown in a demo. And are also available in the git repo.