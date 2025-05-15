# Git Repo klonen

#Git #Dotfiles

## Wie klont man ein Repo?

```bash
git clone url_zu_repository pfad/zu/verzeichnis
```

- Die URL bekommst du, indem du bei GitHub auf den grünen `Code`-Knopf drückst und dann bei Clone SSH auswählst
- Dadurch wird der [[`.git`-Ordner]] erstellt

## Was heißt ein Repo klonen?
- Es heißt alles wird kopiert und es wird eine dauerhafte Kommunikation eingerichtet
- Gits Magie findet im `.git`-Ordner statt; dort werden ua Snapshots unseres Codes gespeichert
- Eine Datei muss im Repo sein, damit Git sie verfolgen kann, aber zB `.zshrc` muss im `~` sein,
- ...die Lösung: [[Symlinks]]
