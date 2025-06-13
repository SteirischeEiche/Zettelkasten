# Git: Remotes und GitHub

#Git #boot.dev

## Remotes
- Ein Remote ist ein externes Repo, das die gleiche Git-Historie wie unser lokales hat
- Ein Remote auf GitHub, das den gemeinsamen Stand des Projekts repräsentiert, nennt man __Origin__
- Mit `git remote add` ordnest du deinem lokalen Repo ein Remote-Repo hinzu
- Dadurch haben wir aber noch nicht den Inhalt des Remote-Repos (nur die Metadaten)
- Mit `git fetch` laden wir das `.git/objects/`-Verzeichnis (des Remotes) in unser lokales Repo runter
- Um die Commits (und damit den Inhalt) zu bekommen, müssen wir mergen:
```bash
git merge origin/branchname
```
## GitHub

- GitHub ist eine Seite für Remote-Repos
- Mit `git push` sendet man lokale Änderungen an das Remote-Repo

### Pull Requests
- Man kann auf GitHub seinen lokalen Branch (mit Änderungen) nicht einfach mergen. Das ist eine Sicherheitsmaßnahme.
- Stattdessen muss man zuerst einen Pull Request machen
- Mit einem PR schlägt man seine Änderungen den anderen vor

---

- Mit `git pull` holst du nicht nur die Metadaten (wie bei `git fetch`) sondern alle Dateien vom Remote-Repo in dein lokales
