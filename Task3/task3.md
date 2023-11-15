# Task 3
This exercise builds on the results of the Task2 from today.

## Goal to achive
We want to improve the playbook by adding many best practices. We also want to increase extensibility by using reusable components

## Task details
* Create a task for uninstalling the apache2 web server in the same role in addition to the installation instructions for the apache2 web server.
* So that the role does not install and uninstall the web server when called, add tags that control the behavior. Use the tags `ìnstall`, `uninstall` and `update` specifically here
* Add a handler in the `webserver` role that restarts the `apache2` service.
* Use this handler in the role so that it is called when the webserver configuration changes.
* Change the webport to `8081` again and check if the handler works http://oc-ansible-schulung-[1-15].centralus.cloudapp.azure.com:8081

## Tips
