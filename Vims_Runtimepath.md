# Vims Runtimepath

#Vim

- `runtimepath` ist eine Vim-Option
- Ihr Wert ist eine (durch Kommata getrennte) Liste aller Verzeichnisse, die Vim nach Ressourcen (zB Wörterbücher und Plugins) durchsucht
- Mit `:echo &runtimepath` kannst du sie in Vim anzeigen lassen

## Inhalt der Liste
- `/home/user/.vim` ist zB dein persönliches Vim-Konfigurationsverzeichnis
- Und `/usr/share/vim/vimfiles` ist das systemweite Verzeichnis für zusätzliche Dateien
