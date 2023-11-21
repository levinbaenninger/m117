# Vererbung

Die Vererbung erfolgt automatisch, und vererbte Berechtigungen werden bei der Erstellung einer Datei oder eines Ordners zugewiesen. Wenn man nicht will, dass eine Datei oder ein Ordner über dieselben Berechtigungen wie der übergeordnete Ordner verfügt, hat man folgende Alternativen:

- Vererbung beenden und kopieren (oder entfernen) von vorhandenen Berechtigungen nach Bedarf.
- Auf den übergeordnete Ordner zugreifen und alle Berechtigungen einstellen, die seine Dateien und Unterordner haben sollen.

## Anzeigen von geerbten Berechtigungen

<procedure>
<step>
    Im Windows-Explorer rechts klicken und dann <ui-path>Eigenschaften</ui-path> auswählen.
</step>
<step>
    Auf der Registerkarte <ui-path>Sicherheit</ui-path> auf <ui-path>Erweitert | Erweiterte Sicherheitseinstellungen</ui-path> klicken. Das Register <ui-path>Berechtigung</ui-path> zeigt die aktuellen Berechtigungen an. Für ererbte Berechtigungen zeigt die Spalte <ui-path>Geerbt von</ui-path> den übergeordneten Ordner an.  Wird die Berechtigung wiederum an andere Ressourcen weitervererbt zeigt die Spalte <ui-path>Anwenden auf</ui-path> an, welche Ressourcenarten die Berechtigung erben.
</step>
</procedure>

## Beenden der Vererbung

Wenn man nicht möchte, dass ein Ordner Berechtigungen von einem übergeordneten Ordner erbt, kann man das an der Stelle (Maske <ui-path>Erweiterte Sicherheitseinstellungen</ui-path>) die Vererbung unterbrechen:

<procedure>
    <step>In der Registerkarte <ui-path>Berechtigungen</ui-path> auf <ui-path>Vererbung deaktivieren</ui-path> klicken.</step>
    <step>Nun hat man die Gelegenheit, Berechtigungen die zuvor geerbt wurden in explizite Berechtigungen zu konvertieren, oder die Berechtigungen zu entfernen und nur die Berechtigungen gelten zu lassen, die man explizit für den Ordner oder die Datei festgelegt hat. Man klickt auf <ui-path>Konvertieren</ui-path> und weist nach Bedarf die erforderlichen Berechtigungen zu, oder man klickt auf <ui-path>Entfernen</ui-path>.</step>
</procedure>

## Besitz

Wenn man die geerbten Berechtigungen entfernt hat und noch keine anderen Berechtigungen zugewiesen wurden, kann niemand auf die Ressourcen zugreifen, mit Ausnahme des Besitzers. Dadurch wird jeder von einer Datei oder einem Ordner ausgesperrt, bis auf den Besitzer. Allerdings haben Administratoren immer noch das Recht, die Ressource in Besitz zu nehmen und unbeschränkten Zugang zu erhalten.

## Wiederherstellen geerbter Berechtigungen

Nach einer gewissen Zeit können die Berechtigungen von Dateien und Unterordnern so stark, von denen des übergeordneten Ordners abweichen, dass es kaum noch möglich ist, den Zugriff effizient zu verwalten.

<procedure>
    <step>Man geht über <ui-path>Eigenschaften | Sicherheit | Erweitert</ui-path> zu den erweiterten Sicherheitseinstellungen.</step>
    <step>Dann geht man auf die Registerkarte <ui-path>Berechtigungen</ui-path> und dort auf <ui-path>Vererbung aktivieren</ui-path>.</step>
    <step>Dort wählt man <ui-path>Alle Berechtigungen für untergeordnete Objekte durch vererbbare Berechtigungen von diesem Objekt ersetzen</ui-path> und klickt auf <ui-path>OK</ui-path>.</step>
    <step>Danach kommt eine Meldung von Windows. Auch diese Bestätigen wir mit <ui-path>Ja</ui-path>.</step>
</procedure>