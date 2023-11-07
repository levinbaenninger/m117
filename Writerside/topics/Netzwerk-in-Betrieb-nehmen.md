# Netzwerk in Betrieb nehmen

Werden VMs ohne Firewall gestartet und Windows 10 erkennt kein Netzwerk, verbleibt die Standardkategorie (Netzwerkprofil) im 
<ui-path>öffentlichen Netz</ui-path>. In diesem Fall sind unter <ui-path>Erweiterte Freigabeeinstellungen ändern</ui-path> die Freigabeoptionen 
für das <ui-path>Öffentliches Netzwerk (aktuelles Profil)</ui-path> relevant:

Hier ändert man die folgenden Einstellungen für das aktuelle Profil:

- Netzwerkerkennung einschalten
- Datei- und Druckerfreigabe aktivieren
- <ui-path>Freigabe des öffentlichen Ordners</ui-path> deaktivieren
- 128-Bit-Verschlüsselung verwenden
- Kennwortgeschütztes Freigaben einschalten (belassen).

Zusätzlich muss man sicherstellen, dass der Dienst <ui-path>Funktionssuche und Ressourcenveröffentlichung</ui-path> aktiviert ist.

**Wichtig**: Diese Einstellungen müssen bei jedem Aufstarten der VM gemacht werden.