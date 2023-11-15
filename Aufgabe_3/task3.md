# Task 3
This exercise builds on the results of exercises 1 and 2.

## Task details
* Extend the existing playbook `web.yml`. The target hosts are still the hosts of the `schulung` group.
  * The server port should now be controlled via the variable `web_port`. With port 8080 as default.
  * The download URL for the web assets should be controlled via the variable `web_download_url`. With the current URL as default.
* If the download of the website does not work, a `home.html` with the content "Content missing" should be displayed instead.
* Make sure again that the playbook is idempotent (0 changes on second execution).
* Specify the server port 8081 when running the playbook and make sure it is used.
* Specify an incorrect download URL when executing the playbook and ensure that the error page is displayed.
