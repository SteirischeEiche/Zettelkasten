# SSH-Agent

#SSH #Linux #Git

## SSH-Agent einrichten
- __Wichtig: GitHub empfiehlt den auf macOS vorinstallierten SSH-Agent zu verwenden, nichts von z.B. Homebrew__
- Zuerst die für den Agenten notwendigen Umgebungsvariablen setzen
- Dann einige Einstellungen vornehmen (in der SSH-Konfigurationsdatei)
- __Achtung: GitHub empfiehlt das Speichern der Passphrase in Apple Keychain. Ich habe das `--apple-use-keychain` weggelassen und die Passphrase stattdessen in KeePassXC gespeichert.__

## Verbindung zu GitHub einrichten
- Den öffentlichen Schlüssel auf github.com eingeben
- Die Verbindung getestet und den Fingerabdruck mit github.com verglichen
- Tipp: Du kannst Signaturen/Fingerabdrücke (die z.B. die Shell ausgibt) mit Strg+F auf der entsprechenden Webseite vergleichen
- Durch den Test wird die Datei `kown_hosts` erstellt. Die IP-Adressen unserer SSH-Verbindungen landen dort.
