# Task 4
This exercise builds on the results of exercises 1, 2 and 3.

## Task details
* Transfer the tasks, variables (defaults) and handlers from the last task to a role called `apache2`.
* Place the role under `roles/apache2` next to the playbook. The playbook will find it there directly.
* Reference this role in the `web.yml` playbook. Override the server port in the playbook to port 80.
* Create the error page as a file this time, it should be part of the role (files).
* The variable names should follow the best practices for role variables.
* Make sure that the functionality is preserved.