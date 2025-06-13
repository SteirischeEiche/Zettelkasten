# Git einstellen

#Git #Dotfiles

- Mit `git config` kannst du die globalen Git-Einstellungen ändern
- Man kann auch projektspezifische Einstellungen machen
- (`git config` ist ein Bsp. für einen Subbefehl)
- Einstellungen werden in der Datei `gitconfig` gespeichert

## GitHub
- Man kann auf GitHub eine private Email-Adresse (einen Alias) einrichten
- Du solltest [[2FA]] für GitHub aktivieren

---

- Daten werden in der `gitconfig` in Key-Wert-Paaren gespeichert
- Es gibt eine `gitconfig` auf mehreren Ebenen: System, global, lokal, worktree
- Global überschreibt System, lokal überschreibt global usw.
