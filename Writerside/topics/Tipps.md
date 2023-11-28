# Tipps

* Die meisten Probleme im Bereich der Dateifreigabe können Sie mit folgenden Massnahmen diagnostizieren und beseitigen:

* **Prüfen Sie die Verbindung zwischen dem Computer, der die Ressourcen freigibt, und dem Computer, dessen Benutzer versucht, auf die freigegebenen Ressourcen zuzugreifen**: Beide Computer müssen an das Netzwerk angeschlossen und mit den richtigen TCP/IP- Einstellungen konfiguriert sein. Bei beiden Computern muss die Firewall so eingerichtet sein,
* dass sie eingehende und ausgehende Verbindungen erlaubt. Auf dem Computer, der Ressourcen freigibt, muss in der Windows- Firewall die Ausnahme für die Datei- und Druckerfreigabe aktiviert sein.

* **Prüfen Sie die erweiterten Freigabeeinstellungen im Netzwerk- und Freigabecenter**: Damit Dateien auf einem Windows-Desktopcomputer erfolgreich freigegeben werden können, muss die Datei- und Druckerfreigabe für das aktive (aktuelle) Netzwerkprofil eingeschaltet sein.

* **Prüfen Sie den Netzwerktyp für das aktive Netzwerk**: Im Netzwerk- und Freigabecenter muss der Netzwerktyp auf beiden Computern richtig eingestellt sein. Ist der Netzwerktyp als öffentliches Netz- werk konfiguriert, sind viele Freigabe- und Verbindungseinstellungen gesperrt und eingeschränkt.

* **Prüfen Sie die Freigabeberechtigungen, die NTFS-Berechtigungen und die Zugriffsflags von Dateien**: Die Freigabeberechtigungen müssen so konfiguriert sein, dass der Benutzer Zugriff erhält. Und die NTFS-Berechtigungen müssen so konfiguriert sein, dass sie dem Benutzer Zugriff gewähren. Zugriffsflags für Dateien müssen gelöscht sein, sodass die Dateien nicht als schreibgeschützt, ausgeblendet oder Systemdateien markiert sind.

* **Der Serverdienst muss laufen, damit Dateien freigegeben werden können**: Prüfen Sie auf dem Computer, der Dateien freigibt, ob der Serverdienst läuft und richtig konfiguriert ist. Normalerweise müsste der Dienst "Server" für den automatischen Start konfiguriert sein und unter dem lokalen Systemkonto laufen. Der Serverdienst setzt voraus, dass ein Server-SMB-Treiber verfügbar ist. Ob diese Voraussetzung erfüllt ist, können Sie auf der Registerkarte Abhängigkeiten im Eigenschaftendialogfeld des Dienstes prüfen.