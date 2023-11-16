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

(optional)
* Add the `templates` folder to the `webserver` role.
* add an `page.j2` file into the templates folder and copy the code from the tip below into it
* Add a task to the role, that uses the template and copies it to `/var/www/html/page.html`
* verify your result: http://oc-ansible-schulung-[1-15].centralus.cloudapp.azure.com:8081/page.html

## Tips
 use the following jinja file (fileextension is: *.j2)
```
<html>
    <body>
        <h1>This server ist listening on Port:{{ webserver_port }}</h1>
    </body>
</html>
```