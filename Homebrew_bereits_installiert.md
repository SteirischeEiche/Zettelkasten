# Homebrew: Bereits installierte Programme installieren

#Homebrew #Terminal

- Wenn du mit Homebrew ein Programm installierst, das bereits installiert ist (zB Git), wird nichts gelöscht
- Dh du hast jetzt zwei Versionen von Git auf deinem Computer (du kannst sie mit `which -a` anzeigen)
- Wenn du den Befehl eingibst, wird standardmäßig die Version von Homebrew ausgeführt
- Das liegt daran, dass das Homebrew-Verzeichnis im PFAD vor `/usr/bin/` steht
- Tatsächlich werden `zshrc`, `zshenv` usw. noch vorm PFAD geladen
- Dh wenn du eine Funktion schriebst, die so heißt wie ein Befehl, wird die Funktion ausgeführt
