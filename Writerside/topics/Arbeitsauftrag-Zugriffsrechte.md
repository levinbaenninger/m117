# Arbeitsauftrag - Zugriffsrechte zulassen/verweigern

Zuerst erstelle ich einen Ordner unter <path>C:\LevinBaenninger\Informatikmodule</path>.  
Die eingestellten Rechte können wie folgt eingesehen werden: <ui-path>Rechtsklick auf Ordner | Eigenschaften | Sicherheit | Erweitert | 
Effektiver Zugriff | `Einen Benutzer auswählen`</ui-path>. Ist in dieser Liste <ui-path>Effektiver Zugriff</ui-path> ein NFTS-Recht *ohne* 
Häkchen gezeigt, verfügt der Nutzer bzw. die Gruppe *nicht* über dieses Recht. 

Man kann auch über die Eingabeaufforderung die Berechtigungen einsehen. Dafür geht man mit der Eingabeaufforderung in den Ordner, hier 
<path>C:\LevinBaenninger</path> und gebe dort folgenden Befehl ein:

```Shell
icacls Informatikmodule
```

Dieser gibt ein etwas kryptischen Output zurück. Dort sieht man die Benutzer und Benutzergruppen mit den jeweiligen Berechtigungen. 

Eine genaue Liste mit den Berechtigungen ist so zu finden:

```Shell
icacls /help
```

## Gruppen und Benutzer einsehen

Unter dem Programm `Computerverwaltung` kann man alle Lokalen Nutzer und Gruppen einsehen: <ui-path>Rechtsklick auf Windowstaste | 
Computerverwaltung | Lokale Benutzer und Gruppen</ui-path>.

Bei dieser VM gibt es einen weiteren Nutzer namens **vmuser**.


## Zugriffsrechte verweigern

Nun wollen wir, dass `vmuser` nicht auf unseren Informatikmodule-Ordner zugreifen kann. Das erreichen wir, indem wir in die Eigenschaften des 
betroffenen Ordners gehen und dort wieder unter den Reiter <ui-path>Sicherheit</ui-path>. Dort gehen wir auf <ui-path>Bearbeiten | 
Hinzufügen</ui-path> und fügen den Nutzer, in diesem Fall `vmuser` ein und verweigern ihm jegliche Rechte über die Checkboxen.

![](chechboxen.png)

Nachdem wir auf <ui-path>Übernehmen</ui-path> klicken, wird und Windows eine Sicherheitsmeldung anzeigen, dass weil, wenn wir die Rechte für eine 
Gruppe ändern, in der wir selbst sind, uns ausschliessen könnten.  
Das ist hier jedoch nicht der Fall und können die Sicherheitsfrage mit <ui-path>Ja</ui-path> beantworten.

### Zugriffsrechte überprüfen

Nun können wir wieder mit dem Befehl

```Shell
icacls Informatikmodule
```

überprüfen, ob die Zugriffsrechte angewendet wurden. 

## Sich selber ausschliessen

Nun wollen wir schauen, was passiert, wenn wir uns selber aus einem Ordner ausschliessen. Im Auftrag müssen wir die Zugriffsrechte, der Gruppe `Authetifizierte Benutzer`, verweigern. Da wir selbst in dieser Gruppe sind, werden wir also ausgeschlossen.

Das Vorgehen ist dasselbe wie oben.

Wenn wir nun versuchen den Ordner zu lesen, bekommen wir eine Fehlermeldung mit folgender Nachricht:

![](keine-berechtigung.png)

Wenn wir hier auf <ui-path>Fortsetzen</ui-path> klicken, schreibt Windows uns in eine Gruppe, sodass wir trotzdem auf den Ordner zugreifen können. Das geschieht jedoch nur, weil wir Admin-Rechte haben. 