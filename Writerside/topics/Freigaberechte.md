# Freigaberechte

_Freigabeberechtigungen_ werden verwendet, wenn ein Benutzer versucht, von einem anderen 
Computer des Netzwerks aus auf eine Datei oder einen Ordner zuzugreifen. 
_Zugriffsberechtigungen_ wirken dagegen immer, ob der Benutzer lokal angemeldet ist oder über 
das Netzwerk einen Remotezugriff auf die Datei oder den Ordner durchführt. Beim Remotezugriff 
werden zuerst die _Freigabeberechtigungen_ angewendet und dann die _Zugriffsberechtigungen_.

Um auf einem Computer eine Ressource freigeben zu können, müssen Sie lokaler Administrator 
sein. Die Freigabe der ersten Ressource bereitet den Computer auf die Freigabe von anderen 
Ressourcen vor und ermöglicht anderen Benutzern die Freigabe von Ressourcen, die ihnen 
gehören oder für die sie über die entsprechenden Zugriffsberechtigungen verfügen.

Freigaben lassen sich mit mehreren Programmen erstellen: 
* **Windows-Explorer**: Alle Ausführungen beziehen sich auf dieses Werkzeug.
* **Computerverwaltung**: Verwenden Sie die Computerverwaltung, wenn Sie auf den Computern, mit denen Sie eine Verbindung herstellen können, Ordner
  freigeben möchten. Wenn Sie in der Strukturdarstellung mit der rechten Maustaste auf Computerverwaltung klicken und Sie dann <ui-path>Verbindung mit
  anderem Computer</ui-path> herstellen auswählen, können Sie die Freigaben von anderen Rechnern einsehen.
* **`Net share`**: Verwenden Sie diesen DOS-Befehl, wenn ein Skript Ordner freigeben soll. `net share /?` zeigt die Syntax des Befehls an. 

Wenn Sie die erste Standardordnerfreigabe auf einem Computer anlegen, erstellt Windows 
standardmässig die Ausnahme für Datei- und Druckerfreigabe in der Windows-Firewall. Diese 
eingehende Ausnahme erlaubt anderen Computern im Netzwerk, SMB-Verkehr (Server Message 
Block) durch die Windows-Firewall zu senden, um auf die Freigabe zuzugreifen. Um das 
zuzulassen, öffnet Windows folgende Ports: 

* **UDP-Port 137**, der für die NetBIOS-Namensauflösung benutzt wird 
* **UDP-Port 138**, der für NetBIOS-Datagrammübertragung und -empfang benutzt wird 
* **TCP-Port 139**, der für den NetBIOS-Sitzungsdienst benutzt wird 
* **Dynamische Ports für ICMPv4 und ICMPv6** (die bei Bedarf für Echoanforderungen benutzt 
werden), warum werden personenbezogene Daten kategorisiert?
