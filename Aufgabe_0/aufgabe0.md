# Aufgabe 0 / Preparation
## Ansbile install

The first task is to install Ansible in an Docker container.
This installation is required for all subsequent tasks.

Ansible step-by-step instructions:

1. Connect to the Linux Server
    ```
	ssh student[01-15]@oc-ansible-schulung-all.centralus.cloudapp.azure.com
    ```
2. Run Ubuntu in a Docker Env
    ```
	docker run -d --name=$USER ubuntu tail -f /dev/null
    ```
3. Connect to the Docker Container
    ```
	docker exec -it $USER bash
    ```
4. Install Python3
    ```
	apt update
    apt install python3
    ```
5. Check if python 3.9 or higher is available
    ```
	python3 --version
    ```
6. Install PIP
    ```
	apt install python3-pip
    ```
7. Check if pip is installed
    ```
	python3 -m pip -V
    ```
8. Install Ansible with pip
    ```
	python3 -m pip install ansible
    ```
9.  Check the Ansible Version
    ```
	ansible --version
    ```


## Getting started with Ansible

* create a folder for the ansbile projekt
* create inside this folder another one called `roles`
* go into `roles` and execute the command
  ```
  ansible-galaxy init helloworld
  ```
* insert a Debug Task inside the newly created role
* create a playbook with the name `site.yml` outside of the `roles` folder
* this `site.yml` should call the `helloworld` role on the localhost with an local connection (no inventory needed)
