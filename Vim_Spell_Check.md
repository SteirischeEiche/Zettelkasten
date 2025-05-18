# Vim Spell Check

#Vim

## Aktivieren
- Mit `:set spell` kannst du Spell Check aktivieren
- Mit `:set spelllang=de_de` stellst du die Sprache ein

## Verwendung
- Mit `]s` und `[s` kannst du zwischen falsch geschriebenen Wörtern hin und her springen
- Mit `zg` kannst du ein als falsch markiertes Wort auf deine eigene Wortliste setzen lassen
- Mit `zw` kannst du ein Wort explizit als falsch markieren (kommt auch auf deine Wortliste)
- Wenn der Cursor auf einem falschen Wort ist, kannst du dir mit `z=` Vorschläge anzeigen lassen

## Wo speichert Vim die Wörterbücher?
### Wörterbücher
- Wenn du `:set spelllang=de_de` eingibst und kein deutsches Wörterbuch installiert ist, fragt dich Vim, ob es eines runterladen soll
- Dann werden eine `.spl`- und eine `.sug`-Datei unter `/opt/homebrew/share/vim/vim*/spell/` abgelegt (wenn du Vim unter macOS mit Homebrew runter geladen hast)
- Die `.sug`-Datei ist für die Vorschläge, die du mit `z=` abrufen kannst
- Achtung: Die `.sug`-Datei kann bei großen Dokumenten die Performance beeinträchtigen

### Eigene Wörterliste (Spellfile)
- Die Wörterlist liegt auch unter `/opt/homebrew/share/vim/vim*/spell/`
- Sie heißt `de.utf-8.add`
- Dort steht pro Zeile ein Wort
- Wenn Vim gestartet wird, kompiliert es diese Datei und erzeugt eine `de.utf-8.add.spl`

## Gute Ressourcen
https://thelinuxcode.com/vim_spell_check/

https://www.vimfromscratch.com/articles/spell-and-grammar-vim
