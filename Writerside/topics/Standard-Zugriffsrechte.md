# Standard-Zugriffsrechte

Im Windows-Explorer kann man sich die aktuell vergebenen Berechtigungen ansehen, indem man eine Datei oder Ordner mit der rechten Maustaste 
anklickt, im Kontextmenü <ui-path>Eigenschaften</ui-path> wählt und dann im `Eigenschaften-Dialogfeld` die Registerkarte Sicherheit anklickt.

Wie aus der Abbildung unten hervorgeht, zeigt die Liste <ui-path>Gruppen- oder Benutzernamen</ui-path> alle Benutzer und Gruppen, die über 
Zugriffsberechtigungen für die ausgewählte Ressource verfügen. Wenn man einen Benutzer oder eine Gruppe auswählt, zeigt die Liste die zugewiesenen 
Berechtigungen. Wird das Häkchen hinter einer Berechtigung abgeblendet dargestellt, bedeutet dies, dass die Berechtigung von einem übergeordneten 
Ordner geerbt wurde. Vererbung wird später besprochen.

In der Liste <ui-path>Berechtigungen für "vmuser"</ui-path> sind alle 6 NFTS-Standard-Zugriffsrechte, die für Ordner gelten ausgeführt:

1. Vollzugriff
2. Ändern
3. Lesen, Ausführen
4. Ordnerinhalt anzeigen
5. Lesen
6. Schreiben

Für Dateien gelten die Gleichen mit Ausnahme von 4. <ui-path>Ordnerinhalt anzeigen</ui-path>. 

![Zugriff](zugriff.png)

Diese decken als Standard die meisten Anwendungsfälle ab. Wir verzichten auf den Einsatz von `Speziellen Berechtigungen`.

Die Berechtigungen werden im Dateisystem in der Zugriffsteuerungsliste (`Access Control List` kurz ACL) der ausgewählten Ressource (Ordner oder 
Datei) gespeichert. Die vererbten Berechtigungen jedoch werden von den übergeordneten Ordnern abgeleitet. Diese werden aber auch auf einer 
bestimmten Stufe in der Dateihierarchie explizit definiert.