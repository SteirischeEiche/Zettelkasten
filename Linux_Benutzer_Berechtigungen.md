# Linux: Benutzer und Berechtigungen

#Terminal #boot.dev

## Benutzer
### Sudo
- `sudo` ist ein Schlüsselwort, das dich einen Befehl als Superuser ausführen lässt
- Um `sudo` benutzen zu können, brauchst du ein Passwort mit Superuser-Privilegien
- `sudo` gibt dir uneingeschränkten Zugriff auf alles! Pass auf, dass du nichts beschädigst. Überprüfe, was genau ein Befehl macht bevor du ihn mit `sudo` ausführst.

## Berechtigungen
- Der String (den du dir zB mit `ls -l` anzeigen lassen kannst) beantwortet zwei Fragen:
0. Um was handelt es sich (zB steht `-` für Datei)?
1. Wer hat die Berechtigung?
2. Welche Berechtigungen hat er?
- Was `drwxr-xr--` bedeutet:

|Verzeichnis|Besitzer|Gruppe|alle|
|-----------|--------|------|----|
|Read       |ja      |ja    |ja  |
|Write      |ja      |nein  |nein|
|Execute    |ja      |ja    |nein|

- Mit `chmod` kannst du die Berichtigungen einer Datei oder eines Verzeichnisses ändern
- Mit `chmod -R` kannst du dies für ein Verzeichnis und seinen gesamten Inhalt rekursiv tun
