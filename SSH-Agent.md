# SSH-Agent

#SSH #Git

## Agenten einrichten
- __Wichtig: GitHub empfiehlt den auf macOS vorinstallierten SSH-Agenten zu benutzen__ (nichts von zB Homebrew)
- Zuerst musst du die für den Agenten nötigen [[Umgebungsvariablen]] setzen
- Dann die SSH-Konfig. einstellen
- __Achtung: Ich habe die Passphrase des privaten Schlüssels nicht in Apple-Keychain gespeichert (wie von GitHub empfohlen) sondern in KeePassXC__

## Verbindung zu GitHub einrichten
- Den öffentlichen Schlüssel auf github.com eingeben
- Verbindung testen und Fingerabdruck mit github.com vergleichen
- Tipp: Du kannst Fingerabdrücke (die zB die Shell ausgibt) mit `Strg+F` mit der entsprechenden Webseite vergleichen
- Durch den Test wird die Datei `known_hosts` erstellt. Die IP-Adressen unserer SSH-Verbindungen landen dort.
