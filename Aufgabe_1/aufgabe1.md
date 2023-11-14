# Aufgabe 1
## Aufgabendetails

* Erzeuge ein Inventory im INI-Format bestehend aus
  * Einem Node `localhost` (der ansible-master)
  * Eine Node `schulung[1-15]` (die Hostnamen der managed nodes) mit der remote host Adresse (ansible_host) `oc-ansible-schulung-[1-15].centralus.cloudapp.azure.com`
  * Einer Gruppe `schulung` die den Node `schulung[1-15]` enthält
  * Hinweis: Unter Vergleich mit https://docs.ansible.com/ansible/latest/user_guide/intro_inventory.html#list-of-behavioral-inventory-parameters

* Für den Zugriff auf localhost soll kein ssh verwenden, setze dafür dort die Hostvariable `ansible_connection=local`
* schulung1 soll sich zunächst mit einem ssh keys authentifizieren, setze dafür dort die Hostvariablen auf `~/.ssh/schulung_rsa`
* Erzeuge eine ansible config unter dem Ansible root Verzeichnis `./ansible.cfg` die zunächst keine aktiven Einträge hat.
  * Erstelle einen Eintrag, der auf das erzeugte Inventory zeigt.
  * Erstelle einen Eintrag, sodass ansible auf dem Zielsystem den User `sysadmin` nutzt.
* Führe einen Ad-Hoc Befehl aus, um die Gruppe `schulung` anzupingen.