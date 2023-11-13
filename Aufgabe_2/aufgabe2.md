# Aufgabe 2
Diese Übung baut auf den Ergebnissen der Aufgabe 1 auf.

## Aufgabendetails
* Erstelle ein Playbook `web.yml` im `ansible` Verzeichnis des Git-Repos.
* Die Webserver sollen auf allen Hosts der `schulung` Gruppe laufen
* Das apt Paket für den Apache Webserver heißt in Ubuntu `apache2` und in RHEL `httpd`.
* (Nur Ubuntu)Installiere außerdem das `unzip` Paket auf den Ubuntu Hosts
* Die Webseite wird als gezipptes Tar-Archiv (.tar.gz) unter https://github.com/schwenne/website/archive/refs/tags/v0.0.1.tar.gz bereitgestellt und soll im Rahmen des Playbooks von dort nach `/var/www/html`  heruntergeladen und entpackt werden.
* Der Server soll auf dem Port 8080 horchen.
  * (Ubuntu) Dazu muss in `/etc/apache2/ports.conf` die Zeile `Listen 80` auf `Listen 8080` angepasst werden.
  * (RHEL) Dazu muss in `/etc/httpd/conf/httpd.conf` die Zeile `Listen 80` auf `Listen 8080` angepasst werden.
* Sorge dafür, dass der `apache2` bzw. `httpd` Service gestarted und enabled ist.
* (Nur RHEL) Damit die Webseite erreichebar ist schalte zunächst den Service `firewalld` aus.
* Führe das Ansible-Playbook auf dem ansible-master aus.
* Beim zweiten Ausführen des Playbooks auf einem bereits bespielten Server soll Ansible 0 Changes melden (d.h. das Playbook ist idempotent).
* Die Webseite soll zum Schluss auf deinem Host-Rechner unter http://{{schulung_ip}}:8080/home.html erreichbar sein.
* Nachdem der Hosts abgeschlossen wurde, ändert den Port auf 8081 und lasst das Playbook erneut laufen. Warum ist der Webserver nicht unter 8081 erreichbar?
