# Aufgabe 4
Diese Übung baut auf den Ergebnissen der Aufgabe 1,2 und 3 auf.

## Aufgabendetails
* Überführe die Tasks, Variablen(defaults) und Handler der letzten Aufgabe in eine Rolle namens `apache2`.
* Lege die Rolle unter `roles/apache2` neben dem Playbook ab. Dort wird sie vom Playbook direkt gefunden.
* Referenziere diese Rolle im `web.yml` Playbook. Übersteuere den Serverport im Playbook auf Port 80.
* Lege die Fehlerseite diesmal als Datei an, sie soll Teil der Rolle (files) sein.
* Die Variablennamen sollen den Best-Practices für Rollen-Variablen folgen.
* Stelle sicher, dass die Funktionalität erhalten bleibt.
