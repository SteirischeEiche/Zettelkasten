# KeePassXC-Browser-Addon

#Keepassxc #Browser

## Native Messaging
- Das KeePassXC-Addon braucht Native Messaging
- Native Messaging ermöglicht es Addons, mit Programmen auf deinem Computer zu kommunizieren
- Es kann ein Sicherheitsrisiko darstellen: Aktiviere es nur, wenn du dem Addon vertraust

### Native Messaging mit LibreWolf
- Zuerst musst du das KeePassXC-Addon in [[LibreWolf]] installieren
- Dann _Browser Integration_ in KeePassXC aktivieren und Firefox auswählen
- Dadurch wird folgendes Verzeichnis erstellt: `~/Library/Application\ Support/Mozilla/NativeMessagingHosts/`
- Laut [LibreWolf Dokumentation](https://librewolf.net/docs/faq/#how-do-i-get-native-messaging-to-work-1) musst du dann einen [[Symlink]] erstellen:
```shell
ln -s ~/Library/Application\ Support/Mozilla/NativeMessagingHosts ~/Library/Application\ Support/LibreWolf/NativeMessagingHosts
```

## Bedienung
- Wenn du in KeePassXC einem Eintrag eine URL hinzufügst (`beispiel.com`), erkennt das Addon beim Einloggen auch Subdomains (`login.beispiel.com`)
