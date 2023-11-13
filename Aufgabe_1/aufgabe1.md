# Aufgabe 1
## Aufgabendetails

* Erzeuge im `./inventory/hosts` ein INI-Inventory bestehend aus
  * Einem Node `localhost` (der ansible-master)
  * Eine Node `schulung1` und `node2` (die Hostnamen der managed nodes)
  * Einer Gruppe `schulung` die beide Nodes `node1` und `node2` enthält
  * Hinweis: Unter Vergleich mit https://docs.ansible.com/ansible/latest/user_guide/intro_inventory.html#list-of-behavioral-inventory-parameters

* Für den Zugriff auf localhost soll kein ssh verwenden, setze dafür dort die Hostvariable `ansible_connection=local`
* schulung1 soll sich zunächst mit den generierten ssh keys authentifizieren, setze dafür dort die Hostvariablen `./id_rsa` (für node2 den Pfad auf node2 ändern)
* Erzeuge eine ansible config unter `./ansible.cfg` die zunächst keine akriven Einträge hat.
  * Erstelle einen Eintrag, der auf das erzeugte Inventory zeigt.
  * Erstelle einen Eintrag, sodass ansible auf dem Zielsystem den User `sysadmin` nutzt.
* Führe einen Ad-Hoc Befehl aus, um den Schulungs-Host anzupingen.
