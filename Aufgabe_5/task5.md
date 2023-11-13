# Task 5
This exercise builds on the results of exercises 1, 2, 3 and 4.

## Task details
* Create a task for uninstalling the apache2 web server in the same role in addition to the installation instructions for the apache2 web server.
* So that the role does not install and uninstall the web server when called, add tags that control the behavior. Use the tags `ìnstall`, `uninstall` and `update` specifically here
* Expand the inventory to include the general variables. These include the webport and the downloadURL
* (RHEL) Modify the task so that the `firewalld` service is no longer stopped, but the port 8080 is permanently opened.
