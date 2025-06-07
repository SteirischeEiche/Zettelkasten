# Linux: Befehle

#Terminal #boot.dev

- `head` gibt die ersten `n` Zeilen aus, `tail` die letzten `n` Zeilen
- Der Befehl `less` macht dasselbe wie `more`, hat aber zusätzliche Funktionen (`less` is `more`)
- `touch` aktualisiert den zuletzt-geändert-Stempel einer Datei
- `touch` ist in Skripten nützlich, weil man damit gewährleisten kann, dass eine Datei existiert ohne sie zu verändern
- `rm -r` löscht ein Verzeichnis und den gesamten Inhalt _rekursiv_
- Rekursiv heißt auf gut Deutsch: "Mach es nochmal bzgl. aller Unterverzeichnisse und deren Inhalt"
- `cp -R` kopiert ein Verzeichnis und dessen gesamten Inhalt rekursiv

### Find
- Mit `find` kannst du Dateien und Verzeichnisse auf deinem Computer finden
- Du kannst auch nach Dateien suchen, die einem Muster entsprechen. ZB kannst du nach allen Plaintext-Dateien in deinem Home-Verzeichnis suchen:
```bash
find ~ -name "*.txt"
```
- `*` ist eine Wildcard (dh ein Platzhalter)

### Grep
- `grep` ist `Strg+F` fürs Terminal
- Es ist sehr mächtig
- Wie man in einer Datei nach einem String sucht:
```bash
grep "hello" words.txt
```
- Du kannst mehrere Dateien auf einmal nach demselben String durchsuchen
- Oder rekursiv in einem Verzeichnis mit: `grep -r "hello" .`
