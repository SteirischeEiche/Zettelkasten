# KeePassXC Sicherheit

#Keepassxc #Security

- Du kannst [[2FA]]-Backup-Codes in den Notizen der Einträge speichern
- Mit einem [[Yubikey]] kannst du Quick Unlock nutzen. D.h. du musst nicht jedes Mal deine Passphrase eingeben.

## Verschlüsselung
- Alles, was du in KeePassXC eingibst, wird verschlüsselt in der `kdbx`-Datei gespeichert
- Wenn du deine Datenbank öffnest, wird sie entschlüsselt und im RAM gespeichert
- Es werden niemals unverschlüsselte Daten auf die Festplatte geschrieben

## Browser-Integration
- Eine URL in KeePassXC zu speichern schützt gegen [[Phishing]], weil es dann nur auf der echten Seite funktioniert
- Wenn du ein Icon herunterlädst, wird die Webseite gepingt

## Datenbank exportieren
- Wenn du deine Datenbank als CSV-Datei exportierst, ist sie _nicht mehr verschlüsselt_
- Daher solltest du die CSV-Datei an einem sehr sicheren Ort speichern

## Datenbank in der Cloud?
- Du könntest deine Datenbank in Filen (oder Nextcloud) hochladen, um sie auf allen Geräten zu haben
- Damit vertraust du deine Datenbank aber Dritten an
- Dann kannst du genauso gut Bitwarden benutzen

## Screenshots
- Screenshots werden standardmäßig verhindert (das kann man temporär unter _View_ -> _Allow Screen Capture_ ausschalten)
