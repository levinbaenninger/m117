# Zugriffsrechte

Auf Windows hängen Sicherheit und Freigabe von zwei Faktoren ab:
- Datenträgerformat
- Computereinstellungen

## Datenträgerformat

Vom Datenträgerformat hängt es ab, welche Sicherheitsoptionen verfügbar sind. Lokale Datenträger können mit dem `FAT`-Dateisystem (`File 
Allocation Table` - FAT16/FAT32) oder dem Dateisystem `NTFS` (New Technology File System) formatiert werden.  
Seit Windows Vista werden Harddisks nur noch mit dem Dateisystem `NTFS` formatiert. USB-Sticks oder externe Harddisks nutzen allerdings oft noch 
das etwas ältere FAT-Format.

### FAT

`FAT` bietet nur eine begrenzte Kontrolle über den Dateizugriff. Dateien können nur als Schreibgeschützt, Verborgen oder System gekennzeichnet 
werden. Diese Flags können zwar für Dateien und Ordner festgelegt werden, aber wer Zugriff auf das FAT-Laufwerk hat, kann diese Einstellungen 
ausser Kraft setzen oder löschen. 

### NFTS

`NFTS` ist der Nachfolger von `FAT` und bietet genauere Kontrolle des Zugriffs auf Dateien und Ordner. Man kann ihnen Berechtigungen vergeben, die 
den Zugriff explizit erlauben oder verbieten. Solche Berechtigungen lassen sich auf Benutzer oder Gruppen vergeben. 