# Shell-Skripten: Zshrc vs. Zshenv

#Shell-Skripten #Zsh

- Wenn du ein Terminal öffnest, startet eine _interaktive_ Shell
- Wenn ein Skript ausgeführt wird, ist das dagegen nicht-interaktiv
- `zshrc` wird _nur für interaktive_ Shells geladen
- Wenn du zB eine selbstgeschriebene Funktion in einem Skript aufrufen willst, musst du sie daher in die `zshenv` schreiben
