# Was ist Git? (Repos und Commits)

#Git #boot.dev

## Repos
- Der 1. Schritt bei einem neuen Projekt ist ein Repository (Repo) zu erstellen
- Ein Repo repräsentiert ein Projekt
- Ein Repo ist ein Ordner, der das Projekt und einen `.git`-Ordner enthält
- Mit `git init` macht man einen Ordner zum Git-Repo
- Alle Commits, Branches usw. werden im `.git`-Verzeichnis gespeichert

## Commits
- Ein Commit ist ein Schnappschuss des Repos zu einem bestimmten Zeitpunkt
- Dh ein Repo ist eine (lange) Liste von Commits
- ...und jeder dieser Commits repräsentiert das _gesamte_ Repo zu einem bestimmten Zeitpunkt
- `git log` zeigt diese Historie an
- Jeder Commit hat einen einzigartigen __Hash__, der ihn identifiziert
- `tree` heißen bei Git Verzeichnisse und `blob` Dateien
- Git speichert einen Schnappschuss der _gesamten_ Datei pro Commit, nicht nur die Änderungen
- Git speichert Autor-Informationen in `gitconfig`, damit es weiß wer einen Commit gemacht hat
