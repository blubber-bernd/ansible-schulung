# Aufgabe 0 / Vorbereitung
## Ansbile installieren

Die erste Aufgabe ist es auf einer frischen Linux VM Ansible zu installieren.
Diese Installation wird für alle folgenden Aufgaben benötigt.

Ansible Step-by-Step Anleitung:

1. Connect to the Linux Server
    ```
	ssh -i ~/.ssh/schulung_rsa sysadmin@13.80.43.82
    ```
2. Check if python 3.9 or higher is available
    ```
	python3 --version
    ```
3. Check if pip is installed
    ```
	python3 -m pip -V
 		if not:
		sudo apt update
		sudo apt install python3-pip
    ```
4. Install Ansible with pip
    ```
	python3 -m pip install ansible
    ```
5. Add the installation path to the linux PATH Variable
    ```
	export PATH=$PATH:/home/sysadmin/.local/bin
    ```
6. Check the Ansible Version
    ```
	ansible --version
    ```
