# Task 2
This exercise builds on the results of exercise 1.

## Task details
* Create a playbook `web.yml` in the `ansible` directory of the Git repo.
* The web servers should run on all hosts of the `training` group
* The apt package for the Apache web server is called `apache2` in Ubuntu and `httpd` in RHEL.
* (Ubuntu only)Also install the `unzip` package on the Ubuntu hosts
* The website is provided as a zipped tar archive (.tar.gz) at https://github.com/schwenne/website/archive/refs/tags/v0.0.1.tar.gz and should be downloaded and unzipped from there to `/var/www/html` as part of the playbook.
* The server should listen on port 8080.
  * (Ubuntu) To do this, the line `Listen 80` in `/etc/apache2/ports.conf` must be adapted to `Listen 8080`.
  * (RHEL) In `/etc/httpd/conf/httpd.conf` the line `Listen 80` must be adapted to `Listen 8080`.
* Make sure that the `apache2` or `httpd` service is started and enabled.
* (RHEL only) To make the website accessible, first turn off the `firewalld` service.
* Execute the Ansible playbook on the ansible-master.
* The second time you run the playbook on a server that is already running, Ansible should report 0 changes (i.e. the playbook is idempotent).
* Finally, the website should be accessible on your host computer at http://{{schulung_ip}}:8080/home.html.
* After the host has been completed, change the port to 8081 and run the playbook again. Why is the web server not accessible at 8081?
