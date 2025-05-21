# SSH-Agent

#SSH #Linux #Git

## SSH-Agent einrichten
- __Wichtig: GitHub empfiehlt den auf macOS vorinstallierten SSH-Agent zu verwenden, nichts von z.B. Homebrew__
- Zuerst die für den Agenten notwendigen Umgebungsvariablen setzen
- Dann einige Einstellungen vornehmen (in der SSH-Konfigurationsdatei)
- __Achtung: GitHub empfiehlt das Speichern der Passphrase in Apple Keychain. Ich habe das `--apple-use-keychain` weggelassen und die Passphrase stattdessen in KeePassXC gespeichert.__
