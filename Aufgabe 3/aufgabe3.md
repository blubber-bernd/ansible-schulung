# Aufgabe 3
Diese Übung baut auf den Ergebnissen der Aufgabe 1 und 2 auf.

## Aufgabendetails
* Erweitere das bestehende Playbook `web.yml`. Die Zielhosts sind weiterhin die Hosts der `schulung` Gruppe.
  * Der Server-Port soll nun über die Variable `web_port` gesteuert werden. Mit Port 8080 als Vorbelegung.
  * Die Download-URL für die Web-Assets soll über die Variable `web_download_url` gesteuert werden. Mit der aktuellen URL als Vorbelegung.
* Falls der Download der Website nicht funktioniert, soll stattdessen eine `home.html` mit dem Inhalt "Content missing" angezeigt werden.
* Stelle wieder sicher, dass das Playbook idempotent ist (0 Changes bei zweiter Ausführung).
* Gib den Serverport 8081 beim Playbook ausführen mit und stelle sicher, dass dieser angewendet wird.
* Gib eine falsche Download-URL beim Playbook ausführen mit und stelle sicher, dass die Fehlerseite ausgespielt wird.
