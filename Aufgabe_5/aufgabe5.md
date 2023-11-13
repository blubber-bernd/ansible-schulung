# Aufgabe 5
Diese Übung baut auf den Ergebnissen der Aufgabe 1,2, 3 und 4 auf.

## Aufgabendetails
* Erstelle neben der Installationsanweisung für den apache2 Webserer einen Task für die Deinstallation in der gleichen Rolle.
* Damit die Rolle beim Aufrufen nicht den Webserver installiert und wieder deinstalliert, füge Tags hinzu, die das Verhalten steuern. Nutze hierbei gezielt die Tags `ìnstall`, `uninstall` und `update`
* Erweitere das Inventory um die allgemeingültigen Variablen. Zu diesen Zählen der webport und die DownloadURL
* (RHEL) Baue den Task so um, dass der Service `firewalld` nicht mehr gestoppt wird, sondern der Port 8080 dauerhaft freigegeben wird.